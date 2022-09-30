---
title: Público API Cambios en Aspose.3D 16.9.0
type: docs
weight: 30
url: /es/net/public-api-changes-in-aspose-3d-16-9-0/
---
**Resumen de contenidos**

- [Importación 3D Escena de la fuente PDF](#PublicAPIChangesinAspose.3D16.9.0-Import3DScenefromtheSourcePDF) 
  - [Añade Aspose.ThreeD. Formatos. Clase PdfLoadOptions](#PublicAPIChangesinAspose.3D16.9.0-AddsAspose.ThreeD.Formats.PdfLoadOptionsClass)
  - [Agrega Aspose.ThreeD.FileFormat y Aspose.ThreeD. Formatos. Clase PdfFormat](#PublicAPIChangesinAspose.3D16.9.0-AddsAspose.ThreeD.FileFormatandAspose.ThreeD.Formats.PdfFormatClass)
- [Guardar una escena 3D en el formato PDF](#PublicAPIChangesinAspose.3D16.9.0-Savea3DSceneinthePDFFormat) 
  - [Agrega Aspose.ThreeD. Formatos. Clase PdfSaveOptions y Aspose.ThreeD. Formatos. Enums PdfLightingScheme/PdfRenderMode](#PublicAPIChangesinAspose.3D16.9.0-AddsAspose.ThreeD.Formats.PdfSaveOptionsclassandAspose.ThreeD.Formats.PdfLightingScheme/PdfRenderModeEnums)
- [Agrega el método triangular en la clase Aspose.ThreeD. Entidades. PolygonModificer](#PublicAPIChangesinAspose.3D16.9.0-AddsTriangulateMethodintheAspose.ThreeD.Entities.PolygonModifierClass)
- [Agrega dos métodos binormales BuildTangenten Aspose.ThreeD. Entidades. Clase PolygonModificer](#PublicAPIChangesinAspose.3D16.9.0-AddstwoBuildTangentBinormalMethodsintheAspose.ThreeD.Entities.PolygonModifierClass)

{{% alert color="primary" %}} 

Este documento describe los cambios al Aspose.3D API de la versión 2.1.0 a 16.9.0, que pueden ser de interés para los desarrolladores de módulos/aplicaciones. Incluye no solo métodos públicos nuevos y actualizados, sino también una descripción de cualquier cambio en el comportamiento detrás de escena en Aspose.3D.

{{% /alert %}} 
### **Importación 3D Escena de la fuente PDF**
Usando la versión reciente (16.9.0) o superior, los desarrolladores pueden recuperar 3D escenas de un archivo de entrada PDF.
#### **Añade Aspose.ThreeD. Formatos. Clase PdfLoadOptions**
Hemos añadido PdfLoadOptions clase. Ayuda a cargar contenido desde el archivo de entrada PDF. Los desarrolladores pueden aplicar la contraseña para los PDF protegidos.

**Escena abierta desde un archivo PDF protegido por contraseña**

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
#### **Agrega Aspose.ThreeD.FileFormat y Aspose.ThreeD. Formatos. Clase PdfFormat**
Hemos agregado una entrada de formato PDF en la clase FileFormat para fines de carga y ahorro. La clase PdfFormat ayuda a manipular PDFs.

{{< highlight "java" >}}

 public static readonly Aspose.ThreeD.Formats.PdfFormat PDF;

{{< /highlight >}}

**Extraer todo el contenido en bruto 3D del archivo PDF**

{{< highlight "java" >}}

 // set PDF file path and password

string path = @"House_Design.pdf";

byte[]password = null;

// extract 3D contents

List<byte[]> contents = FileFormat.PDF.Extract(path, password);

int i = 1;

// iterate through the contents and in separate 3D files

foreach (byte[]content in contents)

{

    string fileName = "3d-" + (i++);

    File.WriteAllBytes(fileName, content);

}

{{< /highlight >}}

**Extraiga todas las escenas 3D y guárdelos en un archivo FBX**

{{< highlight "java" >}}

 // set PDF file path and password

string path = @"House_Design.pdf";

byte[]password = null;

List<Scene> scenes = FileFormat.PDF.ExtractScene(path, password);

int i = 1;

// iterate through the scenes and save in 3D files

foreach (Scene scene in scenes)

{

    string fileName = "3d-" + (i++) + ".fbx";

    scene.Save(fileName, FileFormat.FBX7400ASCII);

}

{{< /highlight >}}
### **Guardar una escena 3D en el formato PDF**
Usando la versión reciente (16.9.0) o superior, los desarrolladores pueden guardar todos los archivos 3D compatibles en el formato PDF.
#### **Agrega Aspose.ThreeD. Formatos. Clase PdfSaveOptions y Aspose.ThreeD. Formatos. Enums PdfLightingScheme/PdfRenderMode**
PdfSaveOptions ayuda a aplicar la configuración antes de guardar en el formato de salida PDF. Los desarrolladores pueden establecer un modo de renderizado y un esquema de iluminación antes de guardar una escena 3D en el formato PDF como se indica a continuación:

**Crear un 3D PDF con un cilindro, y renderizado en modo de ilustración sombreada con iluminación optimizada CAD**

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
### **Agrega el método triangular en la clase Aspose.ThreeD. Entidades. PolygonModificer**
Hemos agregado otra sobrecarga del método Triangulate en la clase PolygonModificer que toma un objeto de clase Scene como parámetro.

**Convertir todos los polígonos a triángulos en el archivo FBX**

{{< highlight "java" >}}

 // load an existing 3D file

Scene scene = new Scene("original.fbx");

// triangulate a scene

PolygonModifier.Triangulate(scene);

// save 3D scene

scene.Save("triangulated.fbx", FileFormat.FBX7400ASCII);

{{< /highlight >}}
### **Agrega dos métodos binormales BuildTangenten Aspose.ThreeD. Entidades. Clase PolygonModificer**
Hemos añadido dos métodos BuildTangentBinormal en la clase PolygonModificer. Un método toma el objeto de clase Scene como un parámetro y otro toma el objeto de clase Mesh como un parámetro.

**Crear datos tangente y binormal para todas las mallas en el archivo FBX**

{{< highlight "java" >}}

 // load an existing 3D file

Scene scene = new Scene("original.fbx");

// triangulate a scene

PolygonModifier.BuildTangentBinormal(scene);

// save 3D scene

scene.Save("output.fbx", FileFormat.FBX7400ASCII);

{{< /highlight >}}
