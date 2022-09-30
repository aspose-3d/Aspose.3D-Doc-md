---
title: Aspose.3D for .NET 20,5 Utgivning
type: docs
weight: 30
url: /sv/net/aspose-3d-for-net-20-5-release-notes/
---
{{% alert color="primary" %}} 

Denna sida innehåller release anteckningar för Aspose.3D for .NET 20.5.

{{% /alert %}} 
## **Förbättringar och förändringar**

|` `**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|THREEDNET-664 |` `JT filer som används LZMA-komprimering stöds inte.|` `Förbättring|
|THREEDNET-502 |` `Förbättra OAP-frågan, lägg till stöd för Material/AssetInfo/Transform.|` `Förbättring|
|THREEDNET-668 |` ` Undantag vid lastning DXF|` `Bug|
|THREEDNET-669 |` `Export reparerade maskor till OBJ kommer att misslycka|` `Bug|
|THREEDNET-670 |` `Node.GetBoundingBox () felvärde.|` `Bug|
|THREEDJAVA-73 |` `Undantag vid konvertering 3D fil till PNG|` `Bug|
## **Offentlig API och bakåts oförenliga förändringar**
- Ändrade signaturen för SelectSingleObject/SelectObjects från**Aspose.ThreeD.Nod**



{{< highlight "java" >}}

 //public Aspose.ThreeD.A3DObject SelectSingleObject(string path)

public object SelectSingleObject(string path)

//public System.Collections.Generic.List<Aspose.ThreeD.A3DObject> SelectObjects(string path)

public System.Collections.Generic.List<object> SelectObjects(string path)

{{< /highlight >}}



**Urvalskod**

{{< highlight "java" >}}

 var scene = new Scene(new Torus());

foreach (BoundingBox bbox in scene.RootNode.SelectObjects("//<BoundingBox>"))

{

     Console.WriteLine($"Found a bbox : {bbox}");

}

{{< /highlight >}}

Detta introduceras av THREEDNET-502 som kan fråga djupare objekt som Material/Texture/AssetInfo/Transform/Verte xElements.

- Fixade ett felfel i**Aspose.ThreeD Profiler.**



{{< highlight "java" >}}

 //Old property:

//public double OveralDepth{ get;set;}



//New property

public double OverallDepth{ get;set;} 

{{< /highlight >}}
