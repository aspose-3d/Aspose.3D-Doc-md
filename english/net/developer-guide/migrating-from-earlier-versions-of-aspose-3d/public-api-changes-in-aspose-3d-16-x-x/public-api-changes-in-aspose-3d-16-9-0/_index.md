---
title: Public API Changes in Aspose.3D 16.9.0
type: docs
weight: 30
url: /net/public-api-changes-in-aspose-3d-16-9-0/
---

**Contents Summary**

- [Import 3D Scene from the Source PDF](#PublicAPIChangesinAspose.3D16.9.0-Import3DScenefromtheSourcePDF) 
  - [Adds Aspose.ThreeD.Formats.PdfLoadOptions Class](#PublicAPIChangesinAspose.3D16.9.0-AddsAspose.ThreeD.Formats.PdfLoadOptionsClass)
  - [Adds Aspose.ThreeD.FileFormat and Aspose.ThreeD.Formats.PdfFormat Class](#PublicAPIChangesinAspose.3D16.9.0-AddsAspose.ThreeD.FileFormatandAspose.ThreeD.Formats.PdfFormatClass)
- [Save a 3D Scene in the PDF Format](#PublicAPIChangesinAspose.3D16.9.0-Savea3DSceneinthePDFFormat) 
  - [Adds Aspose.ThreeD.Formats.PdfSaveOptions class and Aspose.ThreeD.Formats.PdfLightingScheme/PdfRenderMode Enums](#PublicAPIChangesinAspose.3D16.9.0-AddsAspose.ThreeD.Formats.PdfSaveOptionsclassandAspose.ThreeD.Formats.PdfLightingScheme/PdfRenderModeEnums)
- [Adds Triangulate Method in the Aspose.ThreeD.Entities.PolygonModifier Class](#PublicAPIChangesinAspose.3D16.9.0-AddsTriangulateMethodintheAspose.ThreeD.Entities.PolygonModifierClass)
- [Adds two BuildTangentBinormal Methods in the Aspose.ThreeD.Entities.PolygonModifier Class](#PublicAPIChangesinAspose.3D16.9.0-AddstwoBuildTangentBinormalMethodsintheAspose.ThreeD.Entities.PolygonModifierClass)

{{% alert color="primary" %}} 

This document describes changes to the Aspose.3D API from version 2.1.0 to 16.9.0, that may be of interest to module/application developers. It includes not only new and updated public methods, but also a description of any changes in the behavior behind the scenes in Aspose.3D.

{{% /alert %}} 
### **Import 3D Scene from the Source PDF**
Using the recent version (16.9.0) or higher, developers can retrieve 3D scenes from an input PDF file.
#### **Adds Aspose.ThreeD.Formats.PdfLoadOptions Class**
We have added PdfLoadOptions class. It helps in loading content from the input PDF file. Developers may apply password for the protected PDFs.

**Open scene from a password-protected PDF file**

{{< highlight java >}}

 // set path with filename and extension 

string path = @"House_Design.pdf";

// create a new scene

Scene scene = new Scene();

// use loading options and apply password

PdfLoadOptions opt = new PdfLoadOptions() {Password = Encoding.UTF8.GetBytes("password")};

// open scene

scene.Open(path, opt);

{{< /highlight >}}
#### **Adds Aspose.ThreeD.FileFormat and Aspose.ThreeD.Formats.PdfFormat Class**
We have added an entry of PDF format in the FileFormat class for loading and saving purposes. The PdfFormat class helps to manipulate PDFs.

{{< highlight java >}}

 public static readonly Aspose.ThreeD.Formats.PdfFormat PDF;

{{< /highlight >}}

**Extract all raw 3D contents from PDF file**

{{< highlight java >}}

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

**Extract all 3D scenes and save them into FBX file**

{{< highlight java >}}

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
### **Save a 3D Scene in the PDF Format**
Using the recent version (16.9.0) or higher, developers can save all supported 3D files in the PDF format.
#### **Adds Aspose.ThreeD.Formats.PdfSaveOptions class and Aspose.ThreeD.Formats.PdfLightingScheme/PdfRenderMode Enums**
The PdfSaveOptions helps in applying setting before saving in the output PDF format. Developers can set a rendering mode and lighting scheme before saving a 3D scene into the PDF format as below:

**Create a 3D PDF with a cylinder, and rendered in shaded illustration mode with CAD optimized lighting**

{{< highlight java >}}

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
### **Adds Triangulate Method in the Aspose.ThreeD.Entities.PolygonModifier Class**
We have added another overload of Triangulate method in the PolygonModifier class which takes a Scene class object as a parameter.

**Convert all polygons to triangles in the FBX file**

{{< highlight java >}}

 // load an existing 3D file

Scene scene = new Scene("original.fbx");

// triangulate a scene

PolygonModifier.Triangulate(scene);

// save 3D scene

scene.Save("triangulated.fbx", FileFormat.FBX7400ASCII);

{{< /highlight >}}
### **Adds two BuildTangentBinormal Methods in the Aspose.ThreeD.Entities.PolygonModifier Class**
We have added two BuildTangentBinormal methods in the PolygonModifier class. One method takes the Scene class object as a parameter and another one takes the Mesh class object as a parameter.

**Build tangent and binormal data for all meshes in the FBX file**

{{< highlight java >}}

 // load an existing 3D file

Scene scene = new Scene("original.fbx");

// triangulate a scene

PolygonModifier.BuildTangentBinormal(scene);

// save 3D scene

scene.Save("output.fbx", FileFormat.FBX7400ASCII);

{{< /highlight >}}
