---
title: Aspose.3D per Python via .NET 22.9 Note di rilascio
type: docs
weight: 4
url: /it/python-net/aspose-3d-for-python-net-22-9-release-notes/
description: Le note di rilascio dello Aspose.3D per Python via .NET 22.9.
---
{{% alert color="primary" %}}

Questa pagina contiene le informazioni sulle note di rilascio per lo Aspose.3D per lo Python via .NET 22.9.

{{% /alert %}}
## **Miglioramenti e modifiche**

|**Chiave**|**Riassunto**|**Categoria**|
|:- |:- |:- |
|THREEDNET-1232 |Aggiungere il supporto del file system temporaneo interno per l'importatore FBX|Miglioramento|
|THREEDNET-1111 |GLTF l'esportazione non è buona|Correzione di bug|
|THREEDNET-1215 |Quando si importa un file OBJ, un nodo può leggere solo un materiale?|Correzione di bug|
|THREEDNET-1216 |La conversione da GLB a GLB perde le trame|Correzione di bug|
|THREEDNET-1225 |Analizzare i problemi riscontrati nel server app-2022 settembre|Correzione di bug|
|THREEDNET-1227 |Opzioni non supportate nei file ASE: MATERIALE_MOLTO/FISICO/MATERIALE_BRILLA|Correzione di bug|
|THREEDNET-1228 |Eccezione durante l'importazione di file JT: Un elemento con la stessa chiave è già stato aggiunto|Correzione di bug|
|THREEDNET-1230 |STL file con faccia quad non è supportato.|Correzione di bug|
|THREEDNET-1231 |USD non supportato tipo StringVector, LayerOffsetVector|Correzione di bug|


## API modifiche ##


### Aggiunto nuovo metodo in classe `aspose.threed.shading.PbrMaterial`:

{{< highlight "java" >}}
    /**
     * Allow convert other material to PbrMaterial
     * @param material 
     */
    def fromMaterial(material : Type[PbrMaterial]) -> PbrMaterial

{{< /highlight >}}


Questo metodo di utilità consente di convertire altri tipi di materiale in un'istanza PbrMaterial e di prenotare le informazioni il più possibile.


