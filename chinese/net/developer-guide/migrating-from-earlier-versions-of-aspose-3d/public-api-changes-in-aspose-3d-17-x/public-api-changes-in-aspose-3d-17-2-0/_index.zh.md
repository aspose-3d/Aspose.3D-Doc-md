---
title: Aspose.3D 17.2.0中的公共 API 更改
type: docs
weight: 10
url: /zh/net/public-api-changes-in-aspose-3d-17-2-0/
---
**内容摘要**

- [导入DirectX文件](#PublicAPIChangesinAspose.3D17.2.0-ImportingDirectXXFiles)
- [添加 Aspose.ThreeD.Formats.X.XLoadOptions类](#PublicAPIChangesinAspose.3D17.2.0-AddsAspose.ThreeD.Formats.X.XLoadOptionsClass)

{{% alert color="primary" %}} 

本文档介绍了模块/应用程序开发人员可能感兴趣的对 Aspose.3D API 从版本17.1.0到17.2.0的更改。它不仅包括新的和更新的公共方法，还包括对 Aspose.3D 中幕后行为的任何更改的描述。

{{% /alert %}} 
####  **导入DirectX文件**
使用最新版本 (17.02) 或更高版本，开发人员可以导入X文件。将XBinary和XText格式条目添加到导入二进制和ASCII X文件中。

**C#**

{{< highlight "java" >}}

 // XBinary and XText entries are added in the FileFormat class

public static readonly Aspose.ThreeD.FileFormat XBinary;

public static readonly Aspose.ThreeD.FileFormat XText;

// load X file

Scene Xfile = new Scene("3D.x");

{{< /highlight >}}
####  **添加 Aspose.ThreeD.Formats.X.XLoadOptions类**
我们添加了XLoadOptions类。它有助于将X文件导入 Aspose.3D API。

**C#**

{{< highlight "java" >}}

 // XBinary and XText entries are added in the FileFormat class

public static readonly Aspose.ThreeD.FileFormat XBinary;

public static readonly Aspose.ThreeD.FileFormat XText;

// initialize Scene class object

Scene scene = new Scene();

// initialize an object

XLoadOptions loadXOpts = new XLoadOptions();

// load X file

scene.Open( "3DX.x", loadXOpts);

{{< /highlight >}}
