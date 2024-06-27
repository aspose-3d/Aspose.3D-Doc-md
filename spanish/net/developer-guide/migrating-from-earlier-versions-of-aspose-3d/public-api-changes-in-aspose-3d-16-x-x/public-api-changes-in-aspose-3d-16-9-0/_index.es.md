---
title: Público API Cambios en Aspose.3D 16.9.0
type: docs
weight: 30
url: /es/net/public-api-changes-in-aspose-3d-16-9-0/
---
**Resumen de contenidos**

- [Importar escena 3D desde la fuente PDF](#PublicAPIChangesinAspose.3D16.9.0-Import3DScenefromtheSourcePDF) 
[Agrega la clase Aspose.ThreeD.Formats.PdfLoadOptions](#PublicAPIChangesinAspose.3D16.9.0-AddsAspose.ThreeD.Formats.PdfLoadOptionsClass)
[Agrega la clase Aspose.ThreeD.FileFormat y Aspose.ThreeD.Formats.PdfFormat](#PublicAPIChangesinAspose.3D16.9.0-AddsAspose.ThreeD.FileFormatandAspose.ThreeD.Formats.PdfFormatClass)
- [Guardar una escena 3D en el formato PDF](#PublicAPIChangesinAspose.3D16.9.0-Savea3DSceneinthePDFFormat) 
[Agrega la clase Aspose.ThreeD.Formats.PdfSaveOptions y Aspose.ThreeD.Formats.PdfLightingScheme/PdfRenderMode Enums](#PublicAPIChangesinAspose.3D16.9.0-AddsAspose.ThreeD.Formats.PdfSaveOptionsclassandAspose.ThreeD.Formats.PdfLightingScheme/PdfRenderModeEnums)
- [Agrega el método Triangulate en la clase Aspose.ThreeD.Entities.PolygonModifier](#PublicAPIChangesinAspose.3D16.9.0-AddsTriangulateMethodintheAspose.ThreeD.Entities.PolygonModifierClass)
- [Agrega dos métodos BuildTangentBinormal en la clase Aspose.ThreeD.Entities.PolygonModifier](#PublicAPIChangesinAspose.3D16.9.0-AddstwoBuildTangentBinormalMethodsintheAspose.ThreeD.Entities.PolygonModifierClass)

{{% alert color="primary" %}} 

This document describes changes to the Aspose.3D API from version 2.1.0 to 16.9.0, that may be of interest to module/application developers. It includes not only new and updated public methods, but also a description of any changes in the behavior behind the scenes in Aspose.3D.

{{% /alert %}} 
###  **Importar escena 3D desde la fuente PDF**
Utilizando la versión reciente (16.9.0) o superior, los desarrolladores pueden recuperar escenas 3D de un archivo PDF de entrada.
####  **Agrega la clase Aspose.ThreeD.Formats.PdfLoadOptions**
Hemos agregado la clase PdfLoadOptions. Ayuda a cargar contenido desde el archivo PDF de entrada. Los desarrolladores pueden aplicar una contraseña para los PDFs protegidos.

**Abrir escena desde un archivo PDF protegido por contraseña**

{{< highlight "java" >}}

 // set path with filename and extension 

string path = @"House_Design.pdf";

// create a new scene

Scene scene = new Scene();

// use loading options and apply password

PdfLoadOptions opt = new PdfLoadOptions() {Password = Encoding.UTF8.GetBytes("password")};

// open scene

scene.Open(path, opt);

{{< /highlight >}}
####  **Agrega la clase Aspose.ThreeD.FileFormat y Aspose.ThreeD.Formats.PdfFormat**
Hemos añadido una entrada de formato PDF en la clase FileFormat para cargar y guardar. La clase PdfFormat ayuda a manipular archivos PDF.

{{< highlight "java" >}}

 public static readonly Aspose.ThreeD.Formats.PdfFormat PDF;

{{< /highlight >}}

**Extraiga todo el contenido crudo 3D del archivo PDF**

{{< highlight "java" >}}

 // set PDF file path and password

string path = @"House_Design.pdf";

byte[] password = null;

// extract 3D contents

List<byte[]> contents = FileFormat.PDF.Extract(path, password);

int i = 1;

// iterate through the contents and in separate 3D files

foreach (byte[] content in contents)

{

    string fileName = "3d-" + (i++);

    File.WriteAllBytes(fileName, content);

}

{{< /highlight >}}

**Extrae todas las escenas 3D y guárdalos en un archivo FBX**

{{< highlight "java" >}}

 // set PDF file path and password

string path = @"House_Design.pdf";

byte[] password = null;

List<Scene> scenes = FileFormat.PDF.ExtractScene(path, password);

int i = 1;

// iterate through the scenes and save in 3D files

foreach (Scene scene in scenes)

{

    string fileName = "3d-" + (i++) + ".fbx";

    scene.Save(fileName, FileFormat.FBX7400ASCII);

}

{{< /highlight >}}
###  **Guardar una escena 3D en el formato PDF**
Con la versión reciente (16.9.0) o superior, los desarrolladores pueden guardar todos los archivos 3D compatibles en el formato PDF.
####  **Agrega la clase Aspose.ThreeD.Formats.PdfSaveOptions y Aspose.ThreeD.Formats.PdfLightingScheme/PdfRenderMode Enums**
PdfSaveOptions ayuda a aplicar la configuración antes de guardar en el formato de salida PDF. Los desarrolladores pueden establecer un modo de renderizado y un esquema de iluminación antes de guardar una escena 3D en el formato PDF como se muestra a continuación:

**Cree un 3D PDF con un cilindro y renderizado en modo de ilustración sombreada con CAD iluminación optimizada**

{{< highlight "java" >}}

 // create a new scene

Scene scene = new Scene();

// create a cylinder child node

scene.RootNode.CreateChildNode("cylinder", new Cylinder()).Material = new PhongMaterial() { DiffuseColor = new Vector3(Color.DarkCyan)};

// set rendering mode and lighting scheme

PdfSaveOptions opt = new PdfSaveOptions();

opt.LightingScheme = PdfLightingScheme.CAD;

opt.RenderMode = PdfRenderMode.ShadedIllustration;

// save in the PDF format

scene.Save("output.pdf", opt);

{{< /highlight >}}
###  **Agrega el método Triangulate en la clase Aspose.ThreeD.Entities.PolygonModifier**
Hemos agregado otra sobrecarga del método Triangulate en la clase PolygonModificer que toma un objeto de clase Scene como parámetro.

**Convierta todos los polígonos a triángulos en el archivo FBX**

{{< highlight "java" >}}

 // load an existing 3D file

Scene scene = new Scene("original.fbx");

// triangulate a scene

PolygonModifier.Triangulate(scene);

// save 3D scene

scene.Save("triangulated.fbx", FileFormat.FBX7400ASCII);

{{< /highlight >}}
###  **Agrega dos métodos BuildTangentBinormal en la clase Aspose.ThreeD.Entities.PolygonModifier**
Hemos añadido dos métodos BuildTangentBinormal en la clase PolygonModificer. Un método toma el objeto de clase Scene como un parámetro y otro toma el objeto de clase Mesh como un parámetro.

**Construir datos tangentes y binormales para todas las mallas en el archivo FBX**

{{< highlight "java" >}}

 // load an existing 3D file

Scene scene = new Scene("original.fbx");

// triangulate a scene

PolygonModifier.BuildTangentBinormal(scene);

// save 3D scene

scene.Save("output.fbx", FileFormat.FBX7400ASCII);

{{< /highlight >}}
