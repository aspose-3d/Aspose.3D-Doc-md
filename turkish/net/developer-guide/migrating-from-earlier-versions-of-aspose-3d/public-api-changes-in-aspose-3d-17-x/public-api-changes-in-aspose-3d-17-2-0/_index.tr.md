---
title: Public API Changes Aspose.3D 17.2.0
type: docs
weight: 10
url: /tr/net/public-api-changes-in-aspose-3d-17-2-0/
---
**Contents Summary**

- [07mporting DirectX X Files](#PublicAPIChangesinAspose.3D17.2.0-ImportingDirectXXFiles)
- [Dds dds Aspose.ThreeD.Formats.X. Xooadlass ptions lass lass](#PublicAPIChangesinAspose.3D17.2.0-AddsAspose.ThreeD.Formats.X.XLoadOptionsClass)

{{% alert color="primary" %}} 

This belgesi, 17.1.0 sürümünden 17.2.0 'a kadar Aspose.3D API 'teki değişiklikleri açıklar, bu modül/uygulama geliştiricilerine ilgi gösterebilir. It sadece yeni ve güncellenmiş kamu yöntemlerini değil, aynı zamanda Aspose.3D 'deki sahnelerin arkasındaki davranıştaki herhangi bir değişikliğin açıklamasını da içerir.

{{% /alert %}} 
#### **07mporting DirectX X Files**
Son sürümü (17.02) veya daha yüksek olan developers sing, geliştiriciler X dosyalarını içe aktarabilir. Binary he binary ininary ve Xbinary ext format girişleri, ikili ve ASCII X dosyalarını içe aktarmaya eklenir.

**C#**

{{< highlight "java" >}}

 // XBinary and XText entries are added in the FileFormat class

public static readonly Aspose.ThreeD.FileFormat XBinary;

public static readonly Aspose.ThreeD.FileFormat XText;

// load X file

Scene Xfile = new Scene("3D.x");

{{< /highlight >}}
#### **Dds dds Aspose.ThreeD.Formats.X. Xooadlass ptions lass lass**
We Xptions oadOptions sınıfı eklemiştir. It, X dosyalarını Aspose.3D API 'e aktarmaya yardımcı olur.

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
