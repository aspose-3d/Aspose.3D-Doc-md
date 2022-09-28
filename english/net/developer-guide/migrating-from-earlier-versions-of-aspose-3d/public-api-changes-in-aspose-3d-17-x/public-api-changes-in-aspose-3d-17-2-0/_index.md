---
title: Public API Changes in Aspose.3D 17.2.0
type: docs
weight: 10
url: /net/public-api-changes-in-aspose-3d-17-2-0/
---

**Contents Summary**

- [Importing DirectX X Files](#PublicAPIChangesinAspose.3D17.2.0-ImportingDirectXXFiles)
- [Adds Aspose.ThreeD.Formats.X.XLoadOptions Class](#PublicAPIChangesinAspose.3D17.2.0-AddsAspose.ThreeD.Formats.X.XLoadOptionsClass)

{{% alert color="primary" %}} 

This document describes changes to the Aspose.3D API from version 17.1.0 to 17.2.0, that may be of interest to module/application developers. It includes not only new and updated public methods, but also a description of any changes in the behavior behind the scenes in Aspose.3D.

{{% /alert %}} 
#### **Importing DirectX X Files**
Using the recent version (17.02) or higher, developers can import X files. The XBinary and XText format entries are added to import binary and ASCII X files.

**C#**

{{< highlight java >}}

 // XBinary and XText entries are added in the FileFormat class

public static readonly Aspose.ThreeD.FileFormat XBinary;

public static readonly Aspose.ThreeD.FileFormat XText;

// load X file

Scene Xfile = new Scene("3D.x");

{{< /highlight >}}
#### **Adds Aspose.ThreeD.Formats.X.XLoadOptions Class**
We have added XLoadOptions class. It helps in importing X files into Aspose.3D API.

**C#**

{{< highlight java >}}

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
