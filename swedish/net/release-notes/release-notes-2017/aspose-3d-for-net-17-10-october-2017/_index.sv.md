---
title: Aspose.3D for .NET 17,10 – oktober 2017
type: docs
weight: 30
url: /sv/net/aspose-3d-for-net-17-10-october-2017/
---
{{% alert color="primary" %}} 

Denna sida innehåller utgåvans anteckningar för[Aspose.3D for .NET 17,0](https://www.nuget.org/packages/Aspose.3D/17.10.0).

{{% /alert %}} 
## **Andra förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|THREEDNET-292|Lägg till stöd för import av 3MF|Ny funktion|
|THREEDNET-302|OBJ till GLTF - ofullständig återgivning av 3D modell|FelComment|
### **Offentlig API och bakåts oförenliga förändringar**
Se förteckningen över eventuella ändringar i allmänheten API såsom lagts till, bytt namn, Avlägsnade eller förlåtna medlemmar samt eventuella icke-tillbaka-kompatibla förändringar till Aspose.3D for .NET. Om du har farhågor om någon förändring som anges, vänligen ta upp det om[Aspose.3D stödforum](https://forum.aspose.com/c/3d/18).
#### **Lägger till Microsoft3MF-medlem till Aspose.ThreeD.FileFormat och Aspose.ThreeD.FileFormatType klasser**
**C#**

{{< highlight "java" >}}

 /// <summary>

/// Microsoft 3D Manufacturing Format

/// </summary>

public static readonly Aspose.ThreeD.FileFormat Microsoft3MF;



/// <summary>

/// Microsoft 3D Manufacturing Format

/// </summary>

public static readonly Aspose.ThreeD.FileFormatType Microsoft3MF;

{{< /highlight >}}

Autoformatdetektering stöds för 3MF-fil, så utvecklare kan importera det direkt med Scene klass konstruktor utan att uttryckligen ange FileFormat.

**C#**

{{< highlight "java" >}}

 Scene scene = new Scene("sphere_logo.3mf");

{{< /highlight >}}
