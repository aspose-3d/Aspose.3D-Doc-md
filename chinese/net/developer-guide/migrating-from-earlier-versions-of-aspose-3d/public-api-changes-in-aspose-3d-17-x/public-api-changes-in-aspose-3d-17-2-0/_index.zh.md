---
title: Aspose.3D中的公共API变化17.2.0
type: docs
weight: 10
url: /zh/net/public-api-changes-in-aspose-3d-17-2-0/
---
**内容摘要**

- [导入DirectX X文件](#PublicAPIChangesinAspose.3D17.2.0-ImportingDirectXXFiles)
- [添加Aspose.ThreeD.Formats.X.Xloadopons类](#PublicAPIChangesinAspose.3D17.2.0-AddsAspose.ThreeD.Formats.X.XLoadOptionsClass)

{{% alert color="primary" %}} 

本文档介绍了从版本17.1.0到版本17.2.0的Aspose.3D API的更改，这些更改可能是模块/应用程序开发人员感兴趣的。它不仅包括新的和更新的公共方法，还包括对Aspose.3D幕后行为的任何变化的描述。

{{% /alert %}} 
#### **导入DirectX X文件**
使用最新版本 (17.02) 或更高版本，开发人员可以导入X文件。XBinary和XText格式条目被添加到导入二进制文件和ASCII X文件。

**C#**

{{< highlight "java" >}}

 // XBinary and XText entries are added in the FileFormat class

public static readonly Aspose.ThreeD.FileFormat XBinary;

public static readonly Aspose.ThreeD.FileFormat XText;

// load X file

Scene Xfile = new Scene("3D.x");

{{< /highlight >}}
#### **添加Aspose.ThreeD.Formats.X.Xloadopons类**
我们添加了xloadopions类。它有助于将X文件导入Aspose.3D API。

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
