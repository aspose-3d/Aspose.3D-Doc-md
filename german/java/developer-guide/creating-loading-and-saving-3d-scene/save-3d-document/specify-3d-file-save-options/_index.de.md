---
title: Wählen Sie 3D Optionen zum Speichern von Dateien
type: docs
weight: 10
url: /de/java/specify-3d-file-save-options/
description: Es gibt mehrere Überladungen von Scene.save-Methoden, die eine SaveOptions-Instanz akzeptieren.
---
## **3D Optionen zum Speichern von Dateien**
Es gibt mehrere Überladungen von Scene.save-Methoden, die eine SaveOptions-Instanz akzeptieren. Dies sollte eine Instanz einer Klasse sein, die von der SaveOptions-Klasse abgeleitet wurde. Jedes Speicher format verfügt über eine entsprechende Klasse, die Speicher optionen für dieses Speicher format enthält. Beispiels weise gibt es ColladaS ave Options für das Speicher format File Format.COLLADA.
### **Verwendung von Collada Optionen speichern**
Der folgende Code zeigt, wie Sie Speicher optionen festlegen, bevor Sie eine 3D-Datei im Format Collada speichern.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-ColladaSaveOption.java" >}}
### **Verwendung von Discreet3DS Optionen speichern**
Der folgende Code zeigt, wie Sie Speicher optionen festlegen, bevor Sie eine 3D-Datei in ein diskretes 3DS-Format speichern.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-Discreet3DSSaveOption.java" >}}
### **Verwendung der Speicher optionen FBX**
Der folgende Code zeigt, wie Sie Speicher optionen festlegen, bevor Sie eine 3D-Datei im Format FBX speichern.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-FBXSaveOption.java" >}}
### **Verwendung von OBJ Optionen speichern**
Der folgende Code zeigt, wie Sie Speicher optionen festlegen, bevor Sie eine 3D-Datei in ein Obj-Format speichern.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-OBJSaveOption.java" >}}
### **Verwendung von STL Optionen speichern**
Der folgende Code zeigt, wie Sie Speicher optionen festlegen, bevor Sie eine 3D-Datei im Format STL speichern.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-STLSaveOption.java" >}}
### **Verwendung der Speicher optionen U3D**
Der folgende Code zeigt, wie Sie Speicher optionen festlegen, bevor Sie ein Dokument im Format U3D speichern.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-U3DSaveOption.java" >}}
### **Verwendung der Speicher optionen glTF**
{{% alert color="primary" %}} 

Diese Funktion wird von Version 19.8 oder höher unterstützt.

{{% /alert %}} 



Der folgende Code zeigt, wie Sie Speicher optionen festlegen, bevor Sie ein Dokument im Format glTF speichern.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-glTFSaveOption.java" >}}
### **Pretty Print in glTF Optionen speichern**
Sie können auch die setPretty Print-Methode der GLTFSaveOptions-Klasse für den vom Menschen verständlichen JSON-Druck verwenden. Der folgende Code zeigt, wie diese Funktional ität verwendet wird.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-loadsave-SaveOptions-prettyPrintInGltfSaveOption.java" >}}
### **Speichern Sie Abhängigkeiten einer 3D Szene im realen Dateisystem**
Entwickler müssen möglicher weise alle Abhängigkeiten der Szene 3D im realen Dateisystem speichern. Sie können den Pfad eines lokalen Verzeichnisses definieren, im Objekt `MemoryFileSystem` speichern oder Abhängigkeiten einfach verwerfen. Die FileSystem-Eigenschaft wird in den Klassen für alle Speicher optionen hinzugefügt.
#### **Speichern der Material dateien verwerfen**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-DiscardSavingMaterial.java" >}}
#### **Abhängigkeiten im lokalen Verzeichnis speichern**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-SavingDependenciesInLocalDirectory.java" >}}
#### **Abhängigkeiten in der Instanz Memory FileS ystem speichern**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-SavingDependenciesInMemoryFileSystem.java" >}}
### **Verwendung der Google Draco (.DRC) Optionen speichern**
Der folgende Code zeigt, wie Sie Speicher optionen festlegen, bevor Sie ein Modell 3D im Format DRC speichern.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-DRCSaveOption.java" >}}
### **Verwendung von RVM Optionen speichern**
Der folgende Code zeigt, wie Sie Speicher optionen festlegen, bevor Sie ein Modell 3D im Format RVM speichern.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-loadsave-SaveOptions-RVMSaveOptions.java" >}}
