---
title: 3D Optionen zum Speichern von Dateien angeben
type: docs
weight: 10
url: /de/java/specify-3d-file-save-options/
description: Es gibt mehrere Überladungen von Scene.save-Methoden, die eine SaveOptions-Instanz akzeptieren.
---
##  **3D Optionen zum Speichern von Dateien**
Es gibt mehrere Überladungen von Scene.save-Methoden, die eine SaveOptions-Instanz akzeptieren. Dies sollte eine Instanz einer Klasse sein, die von der SaveOptions-Klasse abgeleitet wurde. Jedes Speicher format verfügt über eine entsprechende Klasse, die Speicher optionen für dieses Speicher format enthält. Beispiels weise gibt es ColladaS ave Options für das Speicher format File Format.COLLADA.
###  **Verwendung von Collada Speichere-Optionen**
Der folgende Code zeigt, wie Sie Speicher optionen festlegen, bevor Sie eine 3D-Datei im Collada-Format speichern.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-ColladaSaveOption.java" >}}
###  **Verwendung von Discreet3DS Speichere-Optionen**
Der folgende Code zeigt, wie Sie Speicher optionen festlegen, bevor Sie eine 3D-Datei in ein diskretes 3DS-Format speichern.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-Discreet3DSSaveOption.java" >}}
###  **Verwendung der FBX Speicher optionen**
Der folgende Code zeigt, wie Sie Speicher optionen festlegen, bevor Sie eine 3D-Datei in ein FBX-Format speichern.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-FBXSaveOption.java" >}}
###  **Verwendung von OBJ Speichere-Optionen**
Der folgende Code zeigt, wie Sie Speicher optionen festlegen, bevor Sie eine 3D-Datei in ein Obj-Format speichern.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-OBJSaveOption.java" >}}
###  **Verwendung von STL Speichere-Optionen**
Der folgende Code zeigt, wie Sie Speicher optionen festlegen, bevor Sie eine 3D-Datei im STL-Format speichern.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-STLSaveOption.java" >}}
###  **Verwendung der U3D Speicher optionen**
Der folgende Code zeigt, wie Sie Speicher optionen festlegen, bevor Sie ein Dokument im U3D-Format speichern.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-U3DSaveOption.java" >}}
###  **Verwendung der glTF Speicher optionen**
{{% alert color="primary" %}} 

Diese Funktion wird von Version 19.8 oder höher unterstützt.

{{% /alert %}} 



Der folgende Code zeigt, wie Sie Speicher optionen festlegen, bevor Sie ein Dokument im glTF-Format speichern.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-glTFSaveOption.java" >}}
###  **Pretty Print in glTF Speicher optionen**
Sie können auch die setPretty Print-Methode der GLTFSaveOptions-Klasse für den vom Menschen verständlichen JSON-Druck verwenden. Der folgende Code zeigt, wie diese Funktional ität verwendet wird.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-loadsave-SaveOptions-prettyPrintInGltfSaveOption.java" >}}
###  **Speichern von Abhängigkeiten einer 3D-Szene im realen Dateisystem**
Entwickler müssen möglicher weise alle Abhängigkeiten der 3D-Szene im realen Dateisystem speichern. Sie können den Pfad eines lokalen Verzeichnisses definieren, im `MemoryFileSystem`-Objekt speichern oder einfach Abhängigkeiten verwerfen. Die FileSystem-Eigenschaft wird in den Klassen für alle Speicher optionen hinzugefügt.
####  **Speichern der Material dateien verwerfen**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-DiscardSavingMaterial.java" >}}
####  **Abhängigkeiten im lokalen Verzeichnis speichern**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-SavingDependenciesInLocalDirectory.java" >}}
####  **Abhängigkeiten in der Instanz Memory FileS ystem speichern**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-SavingDependenciesInMemoryFileSystem.java" >}}
###  **Verwendung von Google Draco (.DRC) Optionen speichern**
Der folgende Code zeigt, wie Sie Speicher optionen festlegen, bevor Sie ein 3D-Modell im DRC-Format speichern.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-DRCSaveOption.java" >}}
###  **Verwendung von RVM Speichere-Optionen**
Der folgende Code zeigt, wie Sie Speicher optionen festlegen, bevor Sie ein 3D-Modell im RVM-Format speichern.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-loadsave-SaveOptions-RVMSaveOptions.java" >}}
