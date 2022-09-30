---
title: Aspose.3D for .NET 20.5 Note di rilascio
type: docs
weight: 30
url: /it/net/aspose-3d-for-net-20-5-release-notes/
---
{{% alert color="primary" %}} 

Questa pagina contiene le informazioni sulle note di rilascio per lo Aspose.3D for .NET 20.5.

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
- Modificata la firma di SelectSingleObject/SelectObjects da**Aspose.ThreeD. Nodo**



{{< highlight "java" >}}

 //public Aspose.ThreeD.A3DObject SelectSingleObject(string path)

public object SelectSingleObject(string path)

//public System.Collections.Generic.List<Aspose.ThreeD.A3DObject> SelectObjects(string path)

public System.Collections.Generic.List<object> SelectObjects(string path)

{{< /highlight >}}



**Codice campione**

{{< highlight "java" >}}

 var scene = new Scene(new Torus());

foreach (BoundingBox bbox in scene.RootNode.SelectObjects("//<BoundingBox>"))

{

     Console.WriteLine($"Found a bbox : {bbox}");

}

{{< /highlight >}}

Questo è introdotto da THREEDNET-502 che possono interrogare oggetti più profondi come Material/Texture/AssetInfo/Transform/VertexElements.

- Risolto un errore di battitura**Aspose.ThreeD. Profili. HShape**



{{< highlight "java" >}}

 //Old property:

//public double OveralDepth{ get;set;}



//New property

public double OverallDepth{ get;set;} 

{{< /highlight >}}
