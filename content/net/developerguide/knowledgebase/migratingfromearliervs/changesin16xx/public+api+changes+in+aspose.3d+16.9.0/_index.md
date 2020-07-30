---
title : "Public API Changes in Aspose.3D 16.9.0" 
description : "" 
weight : 20080 
toc : false
type: docs
url: /net/developerguide/knowledgebase/migratingfromearliervs/changesin16xx/public+api+changes+in+aspose.3d+16.9.0/
---

# Aspose.3D for .NET : Public API Changes in Aspose.3D 16.9.0


{{< panel title="Contents Summary" style="primary" >}}
*   [Import 3D Scene from the Source PDF](#import-3d-scene-from-the-source-pdf)
    *   [Adds Aspose.ThreeD.Formats.PdfLoadOptions Class](#adds-aspose.threed.formats.pdfloadoptions-class)
    *   [Adds Aspose.ThreeD.FileFormat and Aspose.ThreeD.Formats.PdfFormat Class](#adds-aspose.threed.fileformat-and-aspose.threed.formats.pdfformat-class)
*   [Save a 3D Scene in the PDF Format](#save-a-3d-scene-in-the-pdf-format)
    *   [Adds Aspose.ThreeD.Formats.PdfSaveOptions class and Aspose.ThreeD.Formats.PdfLightingScheme/PdfRenderMode Enums](#adds-aspose.threed.formats.pdfsaveoptions-class-and-aspose.threed.formats.pdflightingscheme/pdfrendermode-enums)
*   [Adds Triangulate Method in the Aspose.ThreeD.Entities.PolygonModifier Class](#adds-triangulate-method-in-the-aspose.threed.entities.polygonmodifier-class)
*   [Adds two BuildTangentBinormal Methods in the Aspose.ThreeD.Entities.PolygonModifier Class](#adds-two-buildtangentbinormal-methods-in-the-aspose.threed.entities.polygonmodifier-class)
{{< /panel >}}
This document describes changes to the Aspose.3D API from version 2.1.0 to 16.9.0, that may be of interest to module/application developers. It includes not only new and updated public methods, but also a description of any changes in the behavior behind the scenes in Aspose.3D.

### Import 3D Scene from the Source PDF

Using the recent version (16.9.0) or higher, developers can retrieve 3D scenes from an input PDF file.

#### Adds Aspose.ThreeD.Formats.PdfLoadOptions Class

We have added `PdfLoadOptions` class. It helps in loading content from the input PDF file. Developers may apply password for the protected PDFs.

**Open scene from a password-protected PDF file**

{{< code lang="cs" >}}
// set path with filename and extension 
string path = @"House_Design.pdf";
// create a new scene
Scene scene = new Scene();
// use loading options and apply password
PdfLoadOptions opt = new PdfLoadOptions() {Password = Encoding.UTF8.GetBytes("password")};
// open scene
scene.Open(path, opt);
{{< /code >}}

#### Adds Aspose.ThreeD.FileFormat and Aspose.ThreeD.Formats.PdfFormat Class

We have added an entry of PDF format in the `FileFormat` class for loading and saving purposes. The `PdfFormat` class helps to manipulate PDFs.

{{< code lang="cs" >}}
public static readonly Aspose.ThreeD.Formats.PdfFormat PDF;
{{< /code >}}

**Extract all raw 3D contents from PDF file**

{{< code lang="cs" >}}
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
{{< /code >}}

**Extract all 3D scenes and save them into FBX file**

{{< code lang="cs" >}}
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
{{< /code >}}

### Save a 3D Scene in the PDF Format

Using the recent version (16.9.0) or higher, developers can save all supported 3D files in the PDF format.

#### Adds Aspose.ThreeD.Formats.PdfSaveOptions class and Aspose.ThreeD.Formats.PdfLightingScheme/PdfRenderMode Enums

The `PdfSaveOptions` helps in applying setting before saving in the output PDF format. Developers can set a rendering mode and lighting scheme before saving a 3D scene into the PDF format as below:

**Create a 3D PDF with a cylinder, and rendered in shaded illustration mode with CAD optimized lighting**

{{< code lang="cs" >}}
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
{{< /code >}}

### Adds Triangulate Method in the Aspose.ThreeD.Entities.PolygonModifier Class

We have added another overload of `Triangulate` method in the `PolygonModifier` class which takes a `Scene` class object as a parameter.

**Convert all polygons to triangles in the FBX file**

{{< code lang="cs" >}}
// load an existing 3D file
Scene scene = new Scene("original.fbx");
// triangulate a scene
PolygonModifier.Triangulate(scene);
// save 3D scene
scene.Save("triangulated.fbx", FileFormat.FBX7400ASCII);
{{< /code >}}

### Adds two BuildTangentBinormal Methods in the Aspose.ThreeD.Entities.PolygonModifier Class

We have added two `BuildTangentBinormal` methods in the `PolygonModifier` class. One method takes the `Scene` class object as a parameter and another one takes the `Mesh` class object as a parameter.

**Build tangent and binormal data for all meshes in the FBX file**

{{< code lang="cs" >}}
// load an existing 3D file
Scene scene = new Scene("original.fbx");
// triangulate a scene
PolygonModifier.BuildTangentBinormal(scene);
// save 3D scene
scene.Save("output.fbx", FileFormat.FBX7400ASCII);
{{< /code >}}

