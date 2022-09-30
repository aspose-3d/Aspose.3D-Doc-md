---
title: Aspose.3D for Java 20,5 Utgivning
type: docs
weight: 30
url: /sv/java/aspose-3d-for-java-20-5-release-notes/
---
{{% alert color="primary" %}} 

Denna sida innehåller release anteckningar för Aspose.3D for Java 20.5.

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
## **Offentlig API och bakåtkompatibla förändringar**
- Ändrade signaturen för SelectSingleObject/SelectObjects från**Com.aspose. Threed.Node.**



{{< highlight "java" >}}

 //public java.util.ArrayList<com.aspose.threed.A3DObject> com.aspose.threed.Node.selectObjects(java.lang.String) throws com.aspose.threed.ParseException;

public java.util.ArrayList<java.lang.Object> com.aspose.threed.Node.selectObjects(java.lang.String) throws com.aspose.threed.ParseException;

//public com.aspose.threed.A3DObject com.aspose.threed.Node.selectSingleObject(java.lang.String) throws com.aspose.threed.ParseException;

public java.lang.Object com.aspose.threed.Node.selectSingleObject(java.lang.String) throws com.aspose.threed.ParseException;

{{< /highlight >}}


**Urvalskod**

{{< highlight "java" >}}

 Scene scene = new Scene(new Torus());

for(Object bbox : scene.getRootNode().selectObjects("//<BoundingBox>"))

{

     System.out.printf("Found a bbox : %s\n", bbox);

}

{{< /highlight >}}

Detta introduceras av THREEDNET-502 som kan fråga djupare objekt som Material/Texture/AssetInfo/Transform/Verte xElements.

- Fixat en skrivelse i com.a**Spose.3.HShape**



{{< highlight "java" >}}

 //public void com.aspose.threed.HShape.setOveralDepth(double);

public void com.aspose.threed.HShape.setOverallDepth(double);

//public double com.aspose.threed.HShape.getOveralDepth();

public double com.aspose.threed.HShape.getOverallDepth();

{{< /highlight >}}
