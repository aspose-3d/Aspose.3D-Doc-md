---
title: Aspose.3D中的公共API变化16.12.0
type: docs
weight: 10
url: /zh/net/public-api-changes-in-aspose-3d-16-12-0/
---
**内容摘要**

- [添加Aspose.ThreeD。计量类](#PublicAPIChangesinAspose.3D16.12.0-AddsAspose.ThreeD.MeteredClass)
- [导入DXF文件](#PublicAPIChangesinAspose.3D16.12.0-ImportingDXFFiles)

{{% alert color="primary" %}} 

本文档介绍了从版本16.11.0到16.12.0的Aspose.3D API的更改，这些更改可能是模块/应用程序开发人员感兴趣的。它不仅包括新的和更新的公共方法，还包括对Aspose.3D幕后行为的任何变化的描述。

{{% /alert %}} 
### **添加Aspose.ThreeD。计量类**
一种应用计量许可证的方法。

**C#**

{{< highlight "java" >}}

 // initialize a metered license class object

Metered metered = new Metered();

// set public and private keys

metered.SetMeteredKey("your-public-key", "your-private-key");

//Your other code to use Aspose.3D

{{< /highlight >}}
### **导入DXF文件**
使用最新版本 (16.12.0) 或更高版本，开发人员可以导入DXF文件。添加DXF格式条目以用于加载目的。

**C#**

{{< highlight "java" >}}

 // an entry of DXF file in the FileFormat class

public static readonly Aspose.ThreeD.FileFormat DXF;

// load a DXF file

Scene dxfFile = new Scene("wuson.dxf");

{{< /highlight >}}
