---
title: Aspose.3D for .NET 17,5 Utgivningsmeddelanden
type: docs
weight: 80
url: /sv/net/aspose-3d-for-net-17-5-release-notes/
---
{{% alert color="primary" %}} 

Denna sida innehåller utgåvans anteckningar för[Aspose.3D for .NET 17,5](https://www.nuget.org/packages/Aspose.3D/17.5.0).

{{% /alert %}} 
## **Andra förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|THREEDNET-244|Nytt PBR-material för fysiskt baserad återgivning|Ny funktion|
|THREEDNET-250|Tillåt Aspose.3D API importera GLTF 2.0 ASCII filer|Ny funktion|
|THREEDNET-253|Tillåt Aspose.3D API importera GLTF 2.0 Binära filer|Ny funktion|
### **Offentlig API och bakåts oförenliga förändringar**
Se förteckningen över eventuella ändringar i allmänheten API såsom lagts till, bytt namn, Avlägsnade eller förlåtna medlemmar samt eventuella icke-tillbaka-kompatibla förändringar till Aspose.3D for .NET. Om du har farhågor om någon förändring som anges, vänligen ta upp det om[Aspose.3D stödforum](https://forum.aspose.com/c/3d/18).
#### **Lägger till Aspose.ThreeD.Skrivning.**
Den senaste utgåvan av Aspose.3D for .NET API har lagt till stöd för PBR ( fysiskt baserad rendering) ) material. Utvecklare kan tillämpa PBR material för enheter och rendera till 3D modeller.

Detta kodexempel

**.NET, C#**

{{< highlight "java" >}}

 Scene scene = new Scene();

PbrMaterial mat = new PbrMaterial();

mat.MetallicFactor = 0.9;//an almost metal material

mat.RoughnessFactor = 0.9;//material surface is very rough

//create a box that applied this material

var boxNode = scene.RootNode.CreateChildNode("box", new Box());

boxNode.Material = mat;

{{< /highlight >}}
#### **Medlem uppdateringar till Aspose.ThreeD.FileFormat Class.**
Importera GLTF 2.0 (ASCII & Binär) filer till Aspose.3D API, Två medlemmar (GLTF2 och GLTF2_Binary) läggs till Aspose.ThreeD. Filformatklass.

Detta kodexempel visar hur man importerar GLTF 2.0 ASCII eller binärfil:

**.NET, C#**

{{< highlight "java" >}}

 /********************** New Members **********************/

public static readonly Aspose.ThreeD.FileFormat GLTF2;

public static readonly Aspose.ThreeD.FileFormat GLTF2_Binary;



/******************** Import GLTF 2.0 ********************/

//Create a new scene

var s = new Scene();

//Load it as GLTF2, the second argument is optional since Aspose.3D can detect the actual file type

s.Open("test.gltf", FileFormat.GLTF2);

{{< /highlight >}}

