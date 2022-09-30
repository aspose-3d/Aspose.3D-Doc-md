---
title: Aspose.3D for .NET 17.01 Note di rilascio
type: docs
weight: 120
url: /it/net/aspose-3d-for-net-17-01-release-notes/
---
{{% alert color="primary" %}} 

Questa pagina contiene le note di rilascio per[Aspose.3D for .NET 17.1.0](https://www.nuget.org/packages/Aspose.3D/17.1.0).

{{% /alert %}} 
## **Altri miglioramenti e modifiche**

|**Chiave**|**Riassunto**|**Categoria**|
|:- |:- |:- |
|THREEDNET-227|Aggiungere il supporto per l'importazione dei modelli PLY.|Nuova funzionalità|
### **Pubblico API e modifiche incompatibili arretrate**
Vedere l'elenco di eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non retrocompatibile apportata allo Aspose.3D for .NET. Se hai dubbi su eventuali modifiche elencate, sollevalo sul[Forum di supporto Aspose.3D](https://forum.aspose.com/c/3d/18).
#### **Aggiunge una voce in formato PLY nella classe Aspose.ThreeD.FileFormat**
Abbiamo aggiunto una voce PLY (Polygon File Format) per gli scopi di importazione.
#### **Aggiunge Aspose.ThreeD.Formats.PLY.PlyLoadOptions Class**
Specifica le impostazioni di carico per caricare un modello PLY nello Aspose.3D API. Questa classe di opzioni di carico ha solo una proprietà FlipCoordinateSystem, che esiste anche nelle classi di opzioni di carico di altri formati di file.
#### **Aggiunge Aspose.ThreeD. Classe GlobalTransform**
La classe GlobalTransform fornisce esattamente la stessa interfaccia come Transform, ma tutte le sue proprietà sono di sola lettura. È utile per gli scopi della trasformazione globale.
#### **Aggiunge una proprietà GlobalTransform a Aspose.ThreeD.Node Class**
Permette di accedere alla trasformazione globale del nodo. Questo è utile per trasformare la scena nel formato di file personalizzato dell'utente.
#### **Aggiunge la proprietà Polygons a Aspose.ThreeD.Entities.Mesh Class**
Permette di ottenere tutti i poligoni all'interno della mesh, ogni poligono è un array di indice dei vertici poligonali. Prima di questa proprietà, dobbiamo usare la sintassi foreach per enumerare ogni poligono che è inefficiente.
#### **Rimuove il membro CreateStream da Aspose.ThreeD.Formats.IOConfig Class**
Questo è stato contrassegnato come obsoleto nella versione 16.11.0, la nuova interfaccia FileSystem è stata introdotta nella versione 16.11.0 che fornisce più estensibilità.
