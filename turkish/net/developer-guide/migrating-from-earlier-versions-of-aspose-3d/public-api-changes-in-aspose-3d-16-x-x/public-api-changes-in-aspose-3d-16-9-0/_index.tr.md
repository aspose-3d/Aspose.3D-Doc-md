---
title: Kamu API Aspose içinde değişir. 3D 16.9.0
type: docs
weight: 30
url: /tr/net/public-api-changes-in-aspose-3d-16-9-0/
---
**Contents Summary**

- [Import 3D Scene from the Source PDF](#PublicAPIChangesinAspose.3D16.9.0-Import3DScenefromtheSourcePDF) 
-[Aspose ekler. threed. formats. pdfloadoptions sınıfı](#PublicAPIChangesinAspose.3D16.9.0-AddsAspose.ThreeD.Formats.PdfLoadOptionsClass)
-[Aspose ekler. threed. fileformat ve Aspose. threed. formats. pdfformat sınıfı](#PublicAPIChangesinAspose.3D16.9.0-AddsAspose.ThreeD.FileFormatandAspose.ThreeD.Formats.PdfFormatClass)
- [PDF formatında 3D sahnesini kaydedin](#PublicAPIChangesinAspose.3D16.9.0-Savea3DSceneinthePDFFormat) 
-[Aspose ekler. threed. formats. pdfsaveoptions sınıfı ve Aspose. threed. formats. pdflightingscheme/pdfrendermode enums](#PublicAPIChangesinAspose.3D16.9.0-AddsAspose.ThreeD.Formats.PdfSaveOptionsclassandAspose.ThreeD.Formats.PdfLightingScheme/PdfRenderModeEnums)
- [Aspose. threed. entities. polygonmodifier sınıfında triangulate yöntemi ekler](#PublicAPIChangesinAspose.3D16.9.0-AddsTriangulateMethodintheAspose.ThreeD.Entities.PolygonModifierClass)
- [Adds two BuildTangentBinormal Methods in the Aspose.ThreeD.Entities.PolygonModifier Class](#PublicAPIChangesinAspose.3D16.9.0-AddstwoBuildTangentBinormalMethodsintheAspose.ThreeD.Entities.PolygonModifierClass)

{{% alert color="primary" %}} 

This document describes changes to the Aspose.3D API from version 2.1.0 to 16.9.0, that may be of interest to module/application developers. It includes not only new and updated public methods, but also a description of any changes in the behavior behind the scenes in Aspose.3D.

{{% /alert %}} 
###  **Import 3D Scene from the Source PDF**
Using the recent version (16.9.0) or higher, developers can retrieve 3D scenes from an input PDF file.
####  **Aspose ekler. threed. formats. pdfloadoptions sınıfı**
Pdfloadoptions sınıfını ekledik. İçeriğin PDF dosyasından yüklenmesine yardımcı olur. Geliştiriciler korumalı pdf'ler için şifre uygulayabilir.

**Şifre korumalı PDF dosyasından açık sahne**

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
####  **Aspose ekler. threed. fileformat ve Aspose. threed. formats. pdfformat sınıfı**
We have added an entry of PDF format in the FileFormat class for loading and saving purposes. The PdfFormat class helps to manipulate PDFs.

{{< highlight "java" >}}

 public static readonly Aspose.ThreeD.Formats.PdfFormat PDF;

{{< /highlight >}}

**Tüm ham 3D içeriğini PDF dosyasından ayıklayın**

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

**Extract all 3D scenes and save them into FBX file**

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
###  **PDF formatında 3D sahnesini kaydedin**
Son sürümü (16.9.0) veya daha yüksek kullanarak, geliştiriciler tüm desteklenen 3D dosyalarını PDF formatında kaydedebilir.
####  **Aspose ekler. threed. formats. pdfsaveoptions sınıfı ve Aspose. threed. formats. pdflightingscheme/pdfrendermode enums**
The PdfSaveOptions helps in applying setting before saving in the output PDF format. Developers can set a rendering mode and lighting scheme before saving a 3D scene into the PDF format as below:

**Bir silindir ile 3D PDF oluşturun ve CAD optimize edilmiş aydınlatma ile gölgeli illüstrasyon modunda işleyin**

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
###  **Aspose. threed. entities. polygonmodifier sınıfında triangulate yöntemi ekler**
We, bir parametre olarak bir cene cene sınıfı nesneyi alan olyolygongonodifier sınıfında başka bir aşırı yük eklemiştir.

**Tüm poligonları FBX dosyasında üçgenlere dönüştürün**

{{< highlight "java" >}}

 // load an existing 3D file

Scene scene = new Scene("original.fbx");

// triangulate a scene

PolygonModifier.Triangulate(scene);

// save 3D scene

scene.Save("triangulated.fbx", FileFormat.FBX7400ASCII);

{{< /highlight >}}
###  **Adds two BuildTangentBinormal Methods in the Aspose.ThreeD.Entities.PolygonModifier Class**
We, olyolygongonodifier sınıfında iki BuildTangentBinormal yöntemi eklemiştir. One yöntemi Scene sınıfı nesneyi bir parametre olarak alır ve diğeri Mesh sınıfı nesnesini bir parametre olarak alır.

**FBX dosyasındaki tüm ağlar için tanjant ve binormal veriler oluşturun**

{{< highlight "java" >}}

 // load an existing 3D file

Scene scene = new Scene("original.fbx");

// triangulate a scene

PolygonModifier.BuildTangentBinormal(scene);

// save 3D scene

scene.Save("output.fbx", FileFormat.FBX7400ASCII);

{{< /highlight >}}
