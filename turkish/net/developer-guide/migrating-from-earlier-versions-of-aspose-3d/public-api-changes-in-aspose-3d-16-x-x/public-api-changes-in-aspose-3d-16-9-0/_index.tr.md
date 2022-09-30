---
title: Public API Changes Aspose.3D 16.9.0
type: docs
weight: 30
url: /tr/net/public-api-changes-in-aspose-3d-16-9-0/
---
**Contents Summary**

- [Smport 3D cene cene 07ourource PDF](#PublicAPIChangesinAspose.3D16.9.0-Import3DScenefromtheSourcePDF) 
  - [Dds dds Aspose.ThreeD.Formats. dfdfdfoadlass ptions lass lass](#PublicAPIChangesinAspose.3D16.9.0-AddsAspose.ThreeD.Formats.PdfLoadOptionsClass)
  - [Dds dds Aspose.ThreeD. Fileiormat ve Aspose.ThreeD.Formats. dfdfdformat lass lass](#PublicAPIChangesinAspose.3D16.9.0-AddsAspose.ThreeD.FileFormatandAspose.ThreeD.Formats.PdfFormatClass)
- [PDF Format içinde 07ave bir 3D cene cene](#PublicAPIChangesinAspose.3D16.9.0-Savea3DSceneinthePDFFormat) 
  - [Dds dds Aspose.ThreeD.Formats. dfdfSaveOptions class ve Aspose.ThreeD.Formats. dfdfdftingtingchecheme/dfdfdfenderoode Enums](#PublicAPIChangesinAspose.3D16.9.0-AddsAspose.ThreeD.Formats.PdfSaveOptionsclassandAspose.ThreeD.Formats.PdfLightingScheme/PdfRenderModeEnums)
- [Aspose.ThreeD.Entities. olyolygongonodifier lass lass içinde dds dds Triangulate Method](#PublicAPIChangesinAspose.3D16.9.0-AddsTriangulateMethodintheAspose.ThreeD.Entities.PolygonModifierClass)
- [Aspose.ThreeD.Entities. olyolygonModifier lass lass içinde dds dds iki BuildTangentBinormal Methods](#PublicAPIChangesinAspose.3D16.9.0-AddstwoBuildTangentBinormalMethodsintheAspose.ThreeD.Entities.PolygonModifierClass)

{{% alert color="primary" %}} 

Tbelge, 2.1.0 sürümünden 16.9.0 sürümüne Aspose.3D API değişikliklerini açıklar, bu modül/uygulama geliştiricilerine ilgi gösterebilir. It sadece yeni ve güncellenmiş kamu yöntemlerini değil, aynı zamanda Aspose.3D 'deki sahnelerin arkasındaki davranıştaki herhangi bir değişikliğin açıklamasını da içerir.

{{% /alert %}} 
### **Smport 3D cene cene 07ourource PDF**
Developers son sürümü (16.9.0) veya daha yüksek, geliştiriciler 3D görüntülerini PDF dosyasından alabilir.
#### **Dds dds Aspose.ThreeD.Formats. dfdfdfoadlass ptions lass lass**
We Pdfdfoadptions ptions class ekledi. It, PDF dosyasından içerik yüklemede yardımcı olur. Developers korumalı PFs için şifre uygulayabilir.

**Şifre korumalı PDF dosyasından Open sahne**

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
#### **Dds dds Aspose.ThreeD. Fileiormat ve Aspose.ThreeD.Formats. dfdfdformat lass lass**
We, yükleme ve kaydetme amaçlı 07ile. ormat sınıfında PDF formatının bir girişini eklemiştir. The dfdfdformat sınıfı PDFs işlemek için yardımcı olur.

{{< highlight "java" >}}

 public static readonly Aspose.ThreeD.Formats.PdfFormat PDF;

{{< /highlight >}}

**Extract PDF dosyasından tüm ham 3D içerikleri**

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

**07xtract tüm 3D sahneler ve FBX dosyasına kaydedin**

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
### **PDF Format içinde 07ave bir 3D cene cene**
Developers son sürümü (16.9.0) veya daha yüksek, geliştiriciler PDF formatında desteklenen tüm 3D dosyalarını kaydedebilir.
#### **Dds dds Aspose.ThreeD.Formats. dfdfSaveOptions class ve Aspose.ThreeD.Formats. dfdfdftingtingchecheme/dfdfdfenderoode Enums**
To dfdfdfaveOptions PDF formatında çıktıdan tasarruf etmeden önce ayarı uygulamada yardımcı olur. Developers, 3D sahnesini aşağıdaki gibi PDF formatına kaydetmeden önce bir rendering modu ve aydınlatma şeması ayarlayabilir:

**07bir silindir ile 3D PDF reate ve CAD optimize edilmiş aydınlatma ile gölgeli illüstrasyon modunda işlendi**

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
### **Aspose.ThreeD.Entities. olyolygongonodifier lass lass içinde dds dds Triangulate Method**
We, bir parametre olarak bir cene cene sınıfı nesneyi alan olyolygongonodifier sınıfında başka bir aşırı yük eklemiştir.

**FBX dosyasında tüm poligonları üçgenlere yönlendirin**

{{< highlight "java" >}}

 // load an existing 3D file

Scene scene = new Scene("original.fbx");

// triangulate a scene

PolygonModifier.Triangulate(scene);

// save 3D scene

scene.Save("triangulated.fbx", FileFormat.FBX7400ASCII);

{{< /highlight >}}
### **Aspose.ThreeD.Entities. olyolygonModifier lass lass içinde dds dds iki BuildTangentBinormal Methods**
We, olyolygongonodifier sınıfında iki BuildTangentBinormal yöntemi eklemiştir. One yöntemi Scene sınıfı nesneyi bir parametre olarak alır ve diğeri Mesh sınıfı nesnesini bir parametre olarak alır.

**FBX dosyasındaki tüm ağlar için tangent uild tanjant ve binormal veriler**

{{< highlight "java" >}}

 // load an existing 3D file

Scene scene = new Scene("original.fbx");

// triangulate a scene

PolygonModifier.BuildTangentBinormal(scene);

// save 3D scene

scene.Save("output.fbx", FileFormat.FBX7400ASCII);

{{< /highlight >}}
