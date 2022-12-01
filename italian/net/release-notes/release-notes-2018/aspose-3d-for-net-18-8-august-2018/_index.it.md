---
title: Aspose.3D for .NET 18.8-agosto 2018
type: docs
weight: 50
url: /it/net/aspose-3d-for-net-18-8-august-2018/
---
{{% alert color="primary" %}} 

Questa pagina contiene le note di rilascio per[Aspose.3D for .NET 18.8](https://www.nuget.org/packages/Aspose.3D/18.8.0).

{{% /alert %}} 
## **Altri miglioramenti e modifiche**

|**Chiave**|**Riassunto**|**Categoria**|
|:- |:- |:- |
|THREEDNET-409|Esporta i file glTF con compressione draco|Nuova funzione|
|THREEDNET-401|Utilizzare Aspose.3D con Unity3D|Bug|
|THREEDNET-413|Leggi i file COLLADA che fanno riferimento alla stessa cartella|Bug|
### **Pubblico API e modifiche incompatibili arretrate**
Vedere l'elenco di eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non retrocompatibile apportata allo Aspose.3D for .NET. Se hai dubbi su eventuali modifiche elencate, sollevalo sul[Forum di supporto Aspose.3D](https://forum.aspose.com/c/3d).
### **API modifiche**
#### **Aggiunta una nuova proprietà alla classe Aspose.ThreeD.Formats.GLTFSaveOptions:**
{{< highlight "java" >}}

 	bool DracoCompression{ get;set;}

{{< /highlight >}}

Il valore predefinito è vero, quando questo è abilitato impostando su true, l'esportatore glTF 2.0 codificerà la mesh nel formato Google Draco.
