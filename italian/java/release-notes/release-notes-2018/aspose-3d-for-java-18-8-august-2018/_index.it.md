---
title: Aspose.3D for Java 18.8-agosto 2018
type: docs
weight: 50
url: /it/java/aspose-3d-for-java-18-8-august-2018/
---
{{% alert color="primary" %}} 

Questa pagina contiene le note di rilascio per[Aspose.3D for Java 18.8](https://repository.aspose.com/repo/com/aspose/aspose-3d/18.8/).

{{% /alert %}} 
## **Altri miglioramenti e modifiche**

|**Riassunto**|**Categoria**|
|:- |:- |
|Esporta i file glTF con compressione draco|Nuova funzione|
|Ottimizzare il consumo di memoria per gli indici mesh|Miglioramento|
|Utilizzare Aspose.3D con Unity3D|Bug|
|Leggi i file COLLADA che fanno riferimento alla stessa cartella|Bug|

## **Pubblico API e modifiche incompatibili arretrate**

Si prega di visualizzare l'elenco di eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché eventuali modifiche non retrocompatibili apportate allo Aspose.3D for Java API. Se hai dubbi su eventuali modifiche elencate, sollevalo sul[Forum di supporto Aspose.3D](https://forum.aspose.com/c/3d).

## **API modifiche:**

**Aggiunto un nuovo getter/setter a class com.aspose.threed.GLTFSaveOptions:**

{{< highlight "java" >}}

         public bool getDracoCompression();

        public void setDracoCompression(boolean value);

{{< /highlight >}}

Il valore predefinito è vero, quando questo è abilitato impostando su true, l'esportatore glTF 2.0 codificerà la mesh nel formato Google Draco.
