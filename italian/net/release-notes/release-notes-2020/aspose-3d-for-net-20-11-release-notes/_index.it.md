---
title: Aspose.3D for .NET 20.11 Note di rilascio
type: docs
weight: 6
url: /it/net/aspose-3d-for-net-20-11-release-notes/
---
{{% alert color="primary" %}}

Questa pagina contiene le informazioni sulle note di rilascio per lo Aspose.3D for .NET 20.11.

{{% /alert %}}
## **Miglioramenti e modifiche**

|**Chiave**|**Riassunto**|**Categoria**|
|:- |:- |:- |
|THREEDNET-747 |Renderifica le linee edge per i tipi CAD nel renderer web.|Correzione di bug|
|THREEDNET-748 |Migliorare l'illuminazione nel renderer web|Correzione di bug|
|THREEDNET-755 |Attributi del modello non supportati in alcuni file FBX 6.1.|Correzione di bug|
|THREEDNET-757 |Il file PLY con proprietà int64 non è supportato.|Correzione di bug|
|THREEDNET-756 |Il file 3MF esportato utilizzando lo standard più recente non può essere aperto.|Correzione di bug|
|THREEDNET-758 |Il file FBX 6.0 non può essere importato.|Correzione di bug|
|THREEDNET-760 |Migliorare la compatibilità dei file ASE|Correzione di bug|
|THREEDNET-761 |Consentire specificare la codifica per i file di testo basati su 3D.|Miglioramento|
|THREEDNET-762 |Esporta la scena in HTML utilizzando il nostro ultimo renderer.|Nuova funzionalità|
|THREEDNET-763 |Aggiungi il supporto di collada non standard esportato da un esportatore sconosciuto.|Miglioramento|
|THREEDNET-765 |Ottimizzare le prestazioni di caricamento del file binario PLY|Migliorare|
|THREEDNET-768 |Il file binario STL esportato da Rhinoceros non può essere importato.|Correzione di bug|
|THREEDNET-769 |Aggiungere il supporto delle relazioni nel FBX 6.0|Correzione di bug|
|TRHEEDNET-770 |Il carattere di escape errato nel file FBX causerà l'importazione non riuscita dello Aspose.3D.|Correzione di bug|
|THREEDNET-771 |Aggiungere il supporto dati di incorporamento nel FBX|Correzione di bug|


## API modifiche ##


Il cambiamento principale in questa versione è che il file HTML5 esportato non utilizzerà più il vecchio renderer.

Per il rendering viene invece utilizzato un renderer basato su WebAssembly.

Un sacco di bug sono stati risolti in questa versione.

### Aggiunta nuova proprietà alla classe Aspose.ThreeD.Entities.VertexElementUserData:

{{< highlight "java" >}}

        Aspose.ThreeD.Utilities.IArrayList<int> Indices{ get;}

{{< /highlight >}}

Questa proprietà viene aggiunta in modo che i file fbx contengono dati utente indicizzati possano essere importati correttamente.


### Aggiunta nuova proprietà alla classe Aspose.ThreeD.Formats.IOConfig:

{{< highlight "java" >}}

        System.Text.Encoding Encoding{ get;set;}

{{< /highlight >}}

Viene utilizzato per sovrascrivere la codifica interna predefinita durante l'importazione/l'esportazione, in modo da poter controllare manualmente la codifica dei formati basati su testo.