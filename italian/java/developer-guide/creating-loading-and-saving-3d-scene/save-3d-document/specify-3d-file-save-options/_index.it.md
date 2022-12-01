---
title: Specificare 3D Opzioni di salvataggio file
type: docs
weight: 10
url: /it/java/specify-3d-file-save-options/
description: Esistono diversi overload del metodo Scene.save che accettano un'istanza SaveOptions.
---
## **3D Opzioni di salvataggio file**
Esistono diversi overload del metodo Scene.save che accettano un'istanza SaveOptions. Questa dovrebbe essere un'istanza di una classe derivata dalla classe SaveOptions. Ogni formato di salvataggio ha una classe corrispondente che contiene le opzioni di salvataggio per quel formato di salvataggio, ad esempio c' è ColladaSaveOptions per il formato di salvataggio FileFormat.COLLADA.
### **Utilizzo delle opzioni di salvataggio Collada**
Il codice seguente mostra come impostare le opzioni di salvataggio prima di salvare un file 3D in formato Collada.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-ColladaSaveOption.java" >}}
### **Utilizzo delle opzioni di salvataggio Discreet3DS**
Il codice seguente mostra come impostare le opzioni di salvataggio prima di salvare un file 3D in un formato Discreet 3DS.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-Discreet3DSSaveOption.java" >}}
### **Utilizzo delle opzioni di salvataggio FBX**
Il codice seguente mostra come impostare le opzioni di salvataggio prima di salvare un file 3D in un formato FBX.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-FBXSaveOption.java" >}}
### **Utilizzo delle opzioni di salvataggio OBJ**
Il codice seguente mostra come impostare le opzioni di salvataggio prima di salvare un file 3D in un formato Obj.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-OBJSaveOption.java" >}}
### **Utilizzo delle opzioni di salvataggio STL**
Il codice seguente mostra come impostare le opzioni di salvataggio prima di salvare un file 3D in formato STL.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-STLSaveOption.java" >}}
### **Utilizzo delle opzioni di salvataggio U3D**
Il codice seguente mostra come impostare le opzioni di salvataggio prima di salvare un documento in formato U3D.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-U3DSaveOption.java" >}}
### **Utilizzo delle opzioni di salvataggio glTF**
{{% alert color="primary" %}} 

Questa funzione è supportata dalla versione 19.8 o maggiore.

{{% /alert %}} 



Il codice seguente mostra come impostare le opzioni di salvataggio prima di salvare un documento in formato glTF.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-glTFSaveOption.java" >}}
### **PrettyPrint in glTF Opzioni di salvataggio**
È inoltre possibile utilizzare il metodo setPrettyPrint della classe GLTFSaveOptions per la stampa JSON comprensibile per l'uomo. Il codice seguente mostra come utilizzare questa funzionalità.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-loadsave-SaveOptions-prettyPrintInGltfSaveOption.java" >}}
### **Salvare le dipendenze di una scena 3D nel file system reale**
Gli sviluppatori potrebbero richiedere di salvare tutte le dipendenze della scena 3D nel file system reale. Possono definire il percorso di una directory locale, salvare nell'oggetto `MemoryFileSystem` o semplicemente scartare le dipendenze. La proprietà FileSystem viene aggiunta nelle classi di tutte le opzioni di salvataggio.
#### **Scartare il salvataggio dei file materiali**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-DiscardSavingMaterial.java" >}}
#### **Salvare le dipendenze nella directory locale**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-SavingDependenciesInLocalDirectory.java" >}}
#### **Salvare le dipendenze nell'istanza MemoryFileSystem**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-SavingDependenciesInMemoryFileSystem.java" >}}
### **Utilizzo delle opzioni di salvataggio Google Draco (.DRC)**
Il codice seguente mostra come impostare le opzioni di salvataggio prima di salvare un modello 3D in formato DRC.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-DRCSaveOption.java" >}}
### **Utilizzo delle opzioni di salvataggio RVM**
Il codice seguente mostra come impostare le opzioni di salvataggio prima di salvare un modello 3D in formato RVM.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-loadsave-SaveOptions-RVMSaveOptions.java" >}}
