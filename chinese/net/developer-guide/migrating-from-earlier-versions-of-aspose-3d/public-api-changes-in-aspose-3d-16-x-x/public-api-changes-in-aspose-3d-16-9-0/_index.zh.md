---
title: Aspose.3D 16.9.0中的公共 API 更改
type: docs
weight: 30
url: /zh/net/public-api-changes-in-aspose-3d-16-9-0/
---
**内容摘要**

- [从源 PDF 导入 3D 场景](#PublicAPIChangesinAspose.3D16.9.0-Import3DScenefromtheSourcePDF) 
-[添加 Aspose.ThreeD.Formats.PdfLoadOptions类](#PublicAPIChangesinAspose.3D16.9.0-AddsAspose.ThreeD.Formats.PdfLoadOptionsClass)
-[添加 Aspose.ThreeD.FileFormat和 Aspose.ThreeD.Formats.PdfFormat类](#PublicAPIChangesinAspose.3D16.9.0-AddsAspose.ThreeD.FileFormatandAspose.ThreeD.Formats.PdfFormatClass)
- [以 PDF 格式保存 3D 场景](#PublicAPIChangesinAspose.3D16.9.0-Savea3DSceneinthePDFFormat) 
-[添加 Aspose.ThreeD.Formats.PdfSaveOptions类和 Aspose.ThreeD.PdfLightingScheme/PdfRenderMode枚举](#PublicAPIChangesinAspose.3D16.9.0-AddsAspose.ThreeD.Formats.PdfSaveOptionsclassandAspose.ThreeD.Formats.PdfLightingScheme/PdfRenderModeEnums)
- [在 Aspose.ThreeD.Entities.PolygonModifier类中添加三角化方法](#PublicAPIChangesinAspose.3D16.9.0-AddsTriangulateMethodintheAspose.ThreeD.Entities.PolygonModifierClass)
- [在 Aspose.ThreeD.Entities.PolygonModifier类中添加两个BuildTangentBinormal方法](#PublicAPIChangesinAspose.3D16.9.0-AddstwoBuildTangentBinormalMethodsintheAspose.ThreeD.Entities.PolygonModifierClass)

{{% alert color="primary" %}} 

本文档介绍了对 Aspose.3D API 从版本2.1.0到16.9.0的更改，模块/应用程序开发人员可能会感兴趣。它不仅包括新的和更新的公共方法，还包括对 Aspose.3D 中幕后行为的任何更改的描述。

{{% /alert %}} 
###  **从源 PDF 导入 3D 场景**
使用最新版本 (16.9.0) 或更高版本，开发人员可以从输入 PDF 文件检索 3D 场景。
####  **添加 Aspose.ThreeD.Formats.PdfLoadOptions类**
我们添加了PdfLoadOptions类。它有助于从输入 PDF 文件加载内容。开发人员可以为受保护的pdf应用密码。

**从受密码保护的 PDF 文件中打开场景**

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
####  **添加 Aspose.ThreeD.FileFormat和 Aspose.ThreeD.Formats.PdfFormat类**
我们在FileFormat类中添加了 PDF 格式的条目，用于加载和保存目的。PdfFormat类有助于操作pdf。

{{< highlight "java" >}}

 public static readonly Aspose.ThreeD.Formats.PdfFormat PDF;

{{< /highlight >}}

**从 PDF 文件中提取所有原始 3D 内容**

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

**提取所有 3D 场景并将其保存到 FBX 文件中**

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
###  **以 PDF 格式保存 3D 场景**
使用最新版本 (16.9.0) 或更高版本，开发人员可以以 PDF 格式保存所有受支持的 3D 文件。
####  **添加 Aspose.ThreeD.Formats.PdfSaveOptions类和 Aspose.ThreeD.PdfLightingScheme/PdfRenderMode枚举**
PdfSaveOptions有助于在保存为输出 PDF 格式之前应用设置。在将 3D 场景保存为 PDF 格式之前，开发人员可以设置渲染模式和照明方案，如下所示:

**创建带有圆柱体的 3D PDF，并使用 CAD 优化的照明以阴影插图模式渲染**

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
###  **在 Aspose.ThreeD.Entities.PolygonModifier类中添加三角化方法**
我们在polygonmodifidifier类中添加了另一个重载三角测量方法，该方法将场景类对象作为参数。

**将 FBX 文件中的所有多边形转换为三角形**

{{< highlight "java" >}}

 // load an existing 3D file

Scene scene = new Scene("original.fbx");

// triangulate a scene

PolygonModifier.Triangulate(scene);

// save 3D scene

scene.Save("triangulated.fbx", FileFormat.FBX7400ASCII);

{{< /highlight >}}
###  **在 Aspose.ThreeD.Entities.PolygonModifier类中添加两个BuildTangentBinormal方法**
我们在PolygonModifier类中添加了两个BuildTangentBinormal方法。一种方法将场景类对象作为参数，另一种方法将网格类对象作为参数。

**为 FBX 文件中的所有网格构建切线和二项式数据**

{{< highlight "java" >}}

 // load an existing 3D file

Scene scene = new Scene("original.fbx");

// triangulate a scene

PolygonModifier.BuildTangentBinormal(scene);

// save 3D scene

scene.Save("output.fbx", FileFormat.FBX7400ASCII);

{{< /highlight >}}
