---
title: Aspose.3D for .NET 16.11.0 Note di rilascio
type: docs
weight: 20
url: /it/net/aspose-3d-for-net-16-11-0-release-notes/
---
{{% alert color="primary" %}} 

Questa pagina contiene le note di rilascio per[Aspose.3D for .NET 16.11.0](https://www.nuget.org/packages/Aspose.3D/16.11.0).

{{% /alert %}} 
## **Altri miglioramenti e modifiche**

|**Chiave**|**Riassunto**|**Categoria**|
|:- |:- |:- |
|THREEDNET-219|Luce direzionale/spot nel rendering.|Nuova funzionalità|
|THREEDNET-218|Aggiungere una nuova interfaccia per consentire all'utente di esportare le dipendenze nel file system.|Nuova funzionalità|
|THREEDNET-217|Aggiungere il supporto per l'esportazione del testo/binario glTF.|Nuova funzionalità|
|THREEDNET-215|Aggiungere il supporto per l'importazione del binario glTF.|Nuova funzionalità|
|THREEDNET-211|Aggiungere il supporto per l'importazione dello glTF basato sul testo.|Nuova funzionalità|
### **Pubblico API e modifiche incompatibili arretrate**
Vedere l'elenco di eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non retrocompatibile apportata allo Aspose.3D for .NET. Se hai dubbi su eventuali modifiche elencate, sollevalo sul[Forum di supporto Aspose.3D](https://forum.aspose.com/c/3d/18).
### **Aggiunge Aspose.ThreeD.Formats.GLTFLoadOptions Class**
Abbiamo aggiunto la classe GLTFLoadOptions. Definisce le impostazioni sul caricamento di un file glTF.
### **Aggiunge Aspose.ThreeD.Formats.GLTFSaveOptions Class**
Abbiamo aggiunto la classe GLTFSaveOptions. Definisce le impostazioni sul salvataggio di un file glTF.
### **Aggiunge Aspose.ThreeD.Utilities.DummyFileSystem Class**
Ignorerà tutte le dipendenze durante il salvataggio della scena utilizzando le classi di opzioni di salvataggio.
### **Aggiunge Aspose.ThreeD.Utilities.LocalFileSystem Class**
Tutte le dipendenze sono scritte nel file system reale, questo è il valore predefinito di ogni classe di opzione di salvataggio, gli sviluppatori possono usarlo per reindirizzare le dipendenze a una cartella diversa.
### **Aggiunge Aspose.ThreeD.Utilities.MemoryFileSystem Class**
La classe MemoryFileSystem intercetta la scrittura delle dipendenze, ad esempio ottieni il contenuto del file "test.mtl".
### **Aggiunge le voci di estensione e formato GLTF nella classe Aspose.ThreeD.FileFormat**
Abbiamo aggiunto una proprietà Extension e le voci in formato GLTF (GLTF e GLTF _ Binary) per il caricamento e il salvataggio.
#### **Aggiunge una proprietà Extension nella classe Aspose.ThreeD.FileFormatType**
Abbiamo aggiunto una proprietà Extension nella classe FileFormatType per ottenere il nome dell'estensione del formato del file.
### **Aggiunge la proprietà FileSystem nella classe Aspose.ThreeD.Formats.IOConfig**
Abbiamo aggiunto una proprietà FileSystem nella classe IOConfig per scrivere dipendenze.
### **Aggiunge il metodo di entità nella classe Aspose.ThreeD.Node**
Un modo di scelta rapida per l'aggiunta di un'entità a un nodo
