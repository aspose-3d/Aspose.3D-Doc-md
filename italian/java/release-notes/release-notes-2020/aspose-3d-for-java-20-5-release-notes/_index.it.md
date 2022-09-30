---
title: Aspose.3D for Java 20.5 Note di rilascio
type: docs
weight: 30
url: /it/java/aspose-3d-for-java-20-5-release-notes/
---
{{% alert color="primary" %}} 

Questa pagina contiene le informazioni sulle note di rilascio per lo Aspose.3D for Java 20.5.

{{% /alert %}} 
## **Miglioramenti e modifiche**

|` `**Chiave**|**Riassunto**|**Categoria**|
|:- |:- |:- |
|THREEDNET-664 |` `JT file di compressione LZMA utilizzati non sono supportati.|` ` Potenziamento|
|THREEDNET-502 |` ` Migliora la query OAP, aggiungi il supporto per Material/AssetInfo/Transform|` ` Potenziamento|
|THREEDNET-668 |` ` Eccezione sul caricamento del file DXF|` `Bug|
|THREEDNET-669 |` ` Esporta la mesh riparata allo OBJ fallirà|` `Bug|
|THREEDNET-670 |` `Node.GetBoundingBox() valore sbagliato.|` `Bug|
|THREEDJAVA-73 |` ` Eccezione sulla conversione del file 3D in PNG|` `Bug|
## **Pubblico API e modifiche incompatibili arretrate**
- Modificata la firma di SelectSingleObject/SelectObjects da**Com. aspose.threed. Nodo**



{{< highlight "java" >}}

 //public java.util.ArrayList<com.aspose.threed.A3DObject> com.aspose.threed.Node.selectObjects(java.lang.String) throws com.aspose.threed.ParseException;

public java.util.ArrayList<java.lang.Object> com.aspose.threed.Node.selectObjects(java.lang.String) throws com.aspose.threed.ParseException;

//public com.aspose.threed.A3DObject com.aspose.threed.Node.selectSingleObject(java.lang.String) throws com.aspose.threed.ParseException;

public java.lang.Object com.aspose.threed.Node.selectSingleObject(java.lang.String) throws com.aspose.threed.ParseException;

{{< /highlight >}}


**Codice campione**

{{< highlight "java" >}}

 Scene scene = new Scene(new Torus());

for(Object bbox : scene.getRootNode().selectObjects("//<BoundingBox>"))

{

     System.out.printf("Found a bbox : %s\n", bbox);

}

{{< /highlight >}}

Questo è introdotto da THREEDNET-502 che possono interrogare oggetti più profondi come Material/Texture/AssetInfo/Transform/VertexElements.

- Risolto un errore di battitura in com.a**Spose. threed.HShape**



{{< highlight "java" >}}

 //public void com.aspose.threed.HShape.setOveralDepth(double);

public void com.aspose.threed.HShape.setOverallDepth(double);

//public double com.aspose.threed.HShape.getOveralDepth();

public double com.aspose.threed.HShape.getOverallDepth();

{{< /highlight >}}
