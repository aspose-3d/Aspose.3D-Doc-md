---
title: Kamu API Aspose içinde değişir. 3D 17.2.0
type: docs
weight: 10
url: /tr/net/public-api-changes-in-aspose-3d-17-2-0/
---
**Contents Summary**

- [Mpmporting DirectX FFiles](#PublicAPIChangesinAspose.3D17.2.0-ImportingDirectXXFiles)
- [Aspose ekler. threed. formats. x. xloadodosınıfı](#PublicAPIChangesinAspose.3D17.2.0-AddsAspose.ThreeD.Formats.X.XLoadOptionsClass)

{{% alert color="primary" %}} 

This document describes changes to the Aspose.3D API from version 17.1.0 to 17.2.0, that may be of interest to module/application developers. It includes not only new and updated public methods, but also a description of any changes in the behavior behind the scenes in Aspose.3D.

{{% /alert %}} 
####  **Mpmporting DirectX FFiles**
Son sürümü (17.02) veya daha yüksek olan developers sing, geliştiriciler X dosyalarını içe aktarabilir. Binary he binary ininary ve Xbinary ext format girişleri, ikili ve Afiles files files files dosyaları içe aktarmaya eklenir.

**C#**

{{< highlight "java" >}}

 // XBinary and XText entries are added in the FileFormat class

public static readonly Aspose.ThreeD.FileFormat XBinary;

public static readonly Aspose.ThreeD.FileFormat XText;

// load X file

Scene Xfile = new Scene("3D.x");

{{< /highlight >}}
####  **Aspose ekler. threed. formats. x. xloadodosınıfı**
We have added XLoadOptions class. It helps in importing X files into Aspose.3D API.

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
