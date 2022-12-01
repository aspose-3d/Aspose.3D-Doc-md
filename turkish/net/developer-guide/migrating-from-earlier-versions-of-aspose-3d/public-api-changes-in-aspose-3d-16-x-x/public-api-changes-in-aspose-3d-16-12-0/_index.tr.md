---
title: Public API Changes Aspose.3D 16.12.0
type: docs
weight: 10
url: /tr/net/public-api-changes-in-aspose-3d-16-12-0/
---
**Contents Summary**

- [Dds dds Aspose.ThreeD. tered etered tered lass](#PublicAPIChangesinAspose.3D16.12.0-AddsAspose.ThreeD.MeteredClass)
- [07mporting DXF Files](#PublicAPIChangesinAspose.3D16.12.0-ImportingDXFFiles)

{{% alert color="primary" %}} 

Tonun belgesi, 16.11.0 sürümünden 16.12.0 'a Aspose.3D API 'teki değişiklikleri açıklar, bu modül/uygulama geliştiricilerine ilgi gösterebilir. It sadece yeni ve güncellenmiş kamu yöntemlerini değil, aynı zamanda Aspose.3D 'deki sahnelerin arkasındaki davranıştaki herhangi bir değişikliğin açıklamasını da içerir.

{{% /alert %}} 
### **Dds dds Aspose.ThreeD. tered etered tered lass**
Ölçülü bir lisans uygulamak için A way.

**C#**

{{< highlight "java" >}}

 // initialize a metered license class object

Metered metered = new Metered();

// set public and private keys

metered.SetMeteredKey("your-public-key", "your-private-key");

//Your other code to use Aspose.3D

{{< /highlight >}}
### **07mporting DXF Files**
Developers son sürümü (16.12.0) veya daha yüksek, geliştiriciler DXF dosyalarını içe aktarabilir. Yükleme amacıyla 07he DXF format girişi eklenir.

**C#**

{{< highlight "java" >}}

 // an entry of DXF file in the FileFormat class

public static readonly Aspose.ThreeD.FileFormat DXF;

// load a DXF file

Scene dxfFile = new Scene("wuson.dxf");

{{< /highlight >}}
