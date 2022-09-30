---
title: Specificare 3D Opzioni di salvataggio file in C#
linktitle: Specificare 3D Opzioni di salvataggio file
type: docs
weight: 40
url: /it/net/specify-3d-file-save-options/
description: Esistono diverse scene. Salvare gli overload del metodo che accettano un oggetto SaveOptions. Ogni formato di salvataggio ha una classe corrispondente che contiene le opzioni di salvataggio per quel formato di salvataggio.
---
## **Panoramica**

Questo articolo spiega come è possibile salvare i file 3D in diversi formati[Dopo averli caricati in Scene oggetto](https://docs.aspose.com/3d/net/specify-3d-file-load-options/)Utilizzando C#. Caricando e salvando, puoi eseguire il numero di conversioni diverse, ad es.

- Convertire FBX da X in C#
- Convertire fino allo GLTF OBJ nel C#
- Convertire OBJ da X in C#
- Convertire fino allo STL OBJ nel C#
- Convertire fino allo RVM 3DS nel C#

## **3D Opzioni di salvataggio file**
Esistono diversi overload del metodo [`Scene.Save`](https://reference.aspose.com/3d/net/aspose.threed/scene) che accettano un oggetto SaveOptions. Questo dovrebbe essere un oggetto di una classe derivata dalla classe `SaveOptions`. Ogni formato di salvataggio ha una classe corrispondente che contiene le opzioni di salvataggio per quel formato di salvataggio, ad esempio, c' è `ColladaSaveOptions` per il formato di salvataggio `FileFormat.Collada`.
### **Utilizzo delle opzioni di salvataggio Collada**
Il codice C# di seguito mostra come impostare le opzioni di salvataggio prima di salvare un file 3D in formato Collada.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-ColladaSaveOption.cs" >}}
### **Utilizzo delle opzioni di salvataggio Discreet3DS**
Il codice C# di seguito mostra come impostare le opzioni di salvataggio prima di salvare un file 3D in un formato Discreet 3DS.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-Discreet3DSSaveOption.cs" >}}
### **Utilizzo delle opzioni di salvataggio FBX**
Il codice C# di seguito mostra come impostare le opzioni di salvataggio prima di salvare un file 3D in un formato FBX.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-FBXSaveOption.cs" >}}

`FBXSaveOptions` espone anche la proprietà `EnableCompression` che può essere utilizzata per comprimere dati binari di grandi dimensioni nel file FBX. Il valore predefinito di questa proprietà è vero. Di seguito lo snippet di codice spiega come puoi lavorare con questa proprietà durante il salvataggio di una scena.



{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-Save3DScene-Compression.cs" >}}
### **Utilizzo delle opzioni di salvataggio di Obj**
Il codice seguente mostra come impostare le opzioni di salvataggio prima di salvare un file 3D in un formato Obj.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-ObjSaveOption.cs" >}}
### **Utilizzo delle opzioni di salvataggio STL**
Il codice C# di seguito mostra come impostare le opzioni di salvataggio prima di salvare un file 3D in formato STL.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-STLSaveOption.cs" >}}
### **Utilizzo delle opzioni di salvataggio U3D**
Il codice C# di seguito mostra come impostare le opzioni di salvataggio prima di salvare un documento in formato U3D.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-U3DSaveOption.cs" >}}
### **Utilizzo delle opzioni di salvataggio glTF**
{{% alert color="primary" %}} 

Questa funzione è supportata dalla versione 19.8 o maggiore.

{{% /alert %}} 



Il codice C# di seguito mostra come impostare le opzioni di salvataggio prima di salvare un documento in formato glTF.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-glTFSaveOptions.cs" >}}
### **PrettyPrint in glTF Opzioni di salvataggio**
È inoltre possibile utilizzare la proprietà PrettyPrint della classe GLTFSaveOptions per la stampa JSON comprensibile per l'uomo. Il codice seguente mostra come utilizzare questa funzionalità.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-PrettyPrintInGltfSaveOption.cs" >}}
### **Salvare le dipendenze di una scena 3D nel file system reale**
Gli sviluppatori potrebbero richiedere di salvare tutte le dipendenze di scena 3D nel file system reale. Possono definire il percorso di una directory locale, salvare nell'oggetto `MemoryFileSystem` o semplicemente scartare le dipendenze. La proprietà `FileSystem` viene aggiunta nelle classi di tutte le opzioni di salvataggio.
#### **Scartare il salvataggio dei file materiali**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-DiscardSavingMaterial.cs" >}}
#### **Salvare le dipendenze nella directory locale**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-SavingDependenciesInLocalDirectory.cs" >}}
#### **Salvare le dipendenze nell'oggetto MemoryFileSystem**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-SavingDependenciesInMemoryFileSystem.cs" >}}
### **Utilizzo delle opzioni di salvataggio Google Draco (.drc)**
Il codice C# qui sotto mostra come impostare le opzioni di salvataggio prima di salvare un modello 3D in formato DRC.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-DRCSaveOptions.cs" >}}
### **Utilizzo delle opzioni di salvataggio RVM**
Il codice C# qui sotto mostra come impostare le opzioni di salvataggio prima di salvare un modello 3D in formato RVM.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-RVMSaveOptions.cs" >}}
