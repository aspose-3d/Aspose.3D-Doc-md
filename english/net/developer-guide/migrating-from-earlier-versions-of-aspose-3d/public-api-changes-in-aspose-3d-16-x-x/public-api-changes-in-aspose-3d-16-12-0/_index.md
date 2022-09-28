---
title: Public API Changes in Aspose.3D 16.12.0
type: docs
weight: 10
url: /net/public-api-changes-in-aspose-3d-16-12-0/
---

**Contents Summary**

- [Adds Aspose.ThreeD.Metered Class](#PublicAPIChangesinAspose.3D16.12.0-AddsAspose.ThreeD.MeteredClass)
- [Importing DXF Files](#PublicAPIChangesinAspose.3D16.12.0-ImportingDXFFiles)

{{% alert color="primary" %}} 

This document describes changes to the Aspose.3D API from version 16.11.0 to 16.12.0, that may be of interest to module/application developers. It includes not only new and updated public methods, but also a description of any changes in the behavior behind the scenes in Aspose.3D.

{{% /alert %}} 
### **Adds Aspose.ThreeD.Metered Class**
A way to apply a metered license.

**C#**

{{< highlight java >}}

 // initialize a metered license class object

Metered metered = new Metered();

// set public and private keys

metered.SetMeteredKey("your-public-key", "your-private-key");

//Your other code to use Aspose.3D

{{< /highlight >}}
### **Importing DXF Files**
Using the recent version (16.12.0) or higher, developers can import DXF files. The DXF format entry is added for loading purposes.

**C#**

{{< highlight java >}}

 // an entry of DXF file in the FileFormat class

public static readonly Aspose.ThreeD.FileFormat DXF;

// load a DXF file

Scene dxfFile = new Scene("wuson.dxf");

{{< /highlight >}}
