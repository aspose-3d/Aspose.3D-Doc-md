---
title: Specificare 3D Opzioni di salvataggio file
type: docs
weight: 40
url: /it/python-net/specify-3d-file-save-options/
description: Esistono diverse scene. Salvare gli overload del metodo che accettano un oggetto SaveOptions. Ogni formato di salvataggio ha una classe corrispondente che contiene le opzioni di salvataggio per quel formato di salvataggio.
---
## **3D Opzioni di salvataggio file**
Esistono diversi overload del metodo [`Scene.save`](https://reference.aspose.com/3d/net/aspose.threed/scene) che accettano un oggetto `SaveOptions`. Questo dovrebbe essere un oggetto di una classe derivata dalla classe `SaveOptions`. Ogni formato di salvataggio ha una classe corrispondente che contiene le opzioni di salvataggio per quel formato di salvataggio, ad esempio, c' è `ColladaSaveOptions` per il formato di salvataggio `FileFormat.Collada`.
### **Utilizzo delle opzioni di salvataggio Collada**
Il codice seguente mostra come impostare le opzioni di salvataggio prima di salvare un file 3D in formato Collada.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-ColladaSaveOption.py" >}}
### **Utilizzo delle opzioni di salvataggio Discreet3DS**
Il codice seguente mostra come impostare le opzioni di salvataggio prima di salvare un file 3D in un formato Discreet 3DS.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-Discreet3DSSaveOption.py" >}}
### **Utilizzo delle opzioni di salvataggio FBX**
Il codice seguente mostra come impostare le opzioni di salvataggio prima di salvare un file 3D in un formato FBX.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-FBXSaveOption.py" >}}

`FBXSaveOptions` espone anche la proprietà `enable_compression` che può essere utilizzata per comprimere dati binari di grandi dimensioni nel file FBX. Il valore predefinito di questa proprietà è vero. Di seguito lo snippet di codice spiega come puoi lavorare con questa proprietà durante il salvataggio di una scena.



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-Save3DScene-Compression.py" >}}
### **Utilizzo delle opzioni di salvataggio di Obj**
Il codice seguente mostra come impostare le opzioni di salvataggio prima di salvare un file 3D in un formato Obj.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-ObjSaveOption.py" >}}
### **Utilizzo delle opzioni di salvataggio STL**
Il codice seguente mostra come impostare le opzioni di salvataggio prima di salvare un file 3D in formato STL.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-STLSaveOption.py" >}}
### **Utilizzo delle opzioni di salvataggio U3D**
Il codice seguente mostra come impostare le opzioni di salvataggio prima di salvare un documento in formato U3D.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-U3DSaveOption.py" >}}
### **Utilizzo delle opzioni di salvataggio glTF**
{{% alert color="primary" %}} 

Questa funzione è supportata dalla versione 19.8 o maggiore.

{{% /alert %}} 



Il codice seguente mostra come impostare le opzioni di salvataggio prima di salvare un documento in formato glTF.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-glTFSaveOptions.py" >}}
### **PrettyPrint in glTF Opzioni di salvataggio**
È inoltre possibile utilizzare la proprietà PrettyPrint della classe GLTFSaveOptions per la stampa JSON comprensibile per l'uomo. Il codice seguente mostra come utilizzare questa funzionalità.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-PrettyPrintInGltfSaveOption.py" >}}
### **Salvare le dipendenze di una scena 3D nel file system reale**
Gli sviluppatori potrebbero richiedere di salvare tutte le dipendenze di scena 3D nel file system reale. Possono definire il percorso di una directory locale, salvare nell'oggetto MemoryFileSystem o semplicemente scartare le dipendenze. La proprietà FileSystem viene aggiunta nelle classi di tutte le opzioni di salvataggio.
#### **Scartare il salvataggio dei file materiali**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-DiscardSavingMaterial.py" >}}
#### **Salvare le dipendenze nella directory locale**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-SavingDependenciesInLocalDirectory.py" >}}
#### **Salvare le dipendenze nell'oggetto MemoryFileSystem**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-SavingDependenciesInMemoryFileSystem.py" >}}
### **Utilizzo delle opzioni di salvataggio Google Draco (.drc)**
Il codice seguente mostra come impostare le opzioni di salvataggio prima di salvare un modello 3D in formato DRC.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-DRCSaveOptions.py" >}}
### **Utilizzo delle opzioni di salvataggio RVM**
Il codice seguente mostra come impostare le opzioni di salvataggio prima di salvare un modello 3D in formato RVM.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-RVMSaveOptions.py" >}}
