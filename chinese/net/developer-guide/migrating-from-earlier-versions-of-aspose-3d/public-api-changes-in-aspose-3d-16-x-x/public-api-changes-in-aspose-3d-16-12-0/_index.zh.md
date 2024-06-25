---
title: Aspose 中的公共 API 更改。3D 16.12.0
type: docs
weight: 10
url: /zh/net/public-api-changes-in-aspose-3d-16-12-0/
---
**内容摘要**

- [添加 Aspose.ThreeD.Metered类](#PublicAPIChangesinAspose.3D16.12.0-AddsAspose.ThreeD.MeteredClass)
- [正在导入 DXF 个文件](#PublicAPIChangesinAspose.3D16.12.0-ImportingDXFFiles)

{{% alert color="primary" %}} 

本文档介绍了对 Aspose.3D API 从版本16.11.0到16.12.0的更改，模块/应用程序开发人员可能会感兴趣。它不仅包括新的和更新的公共方法，还包括对 Aspose.3D 中幕后行为的任何更改的描述。

{{% /alert %}} 
###  **添加 Aspose.ThreeD.Metered类**
一种应用计量许可证的方法。

**C#**

{{< highlight "java" >}}

 // initialize a metered license class object

Metered metered = new Metered();

// set public and private keys

metered.SetMeteredKey("your-public-key", "your-private-key");

//Your other code to use Aspose.3D

{{< /highlight >}}
###  **正在导入 DXF 个文件**
使用最新版本 (16.12.0) 或更高版本，开发人员可以导入 DXF 文件。DXF 格式条目是为了加载而添加的。

**C#**

{{< highlight "java" >}}

 // an entry of DXF file in the FileFormat class

public static readonly Aspose.ThreeD.FileFormat DXF;

// load a DXF file

Scene dxfFile = new Scene("wuson.dxf");

{{< /highlight >}}
