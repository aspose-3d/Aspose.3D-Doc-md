---
title: 3D Optionen zum Speichern von Dateien angeben
type: docs
weight: 40
url: /de/python-net/specify-3d-file-save-options/
description: Es gibt mehrere Scene.Save-Methoden überladungen, die ein SaveOptions-Objekt akzeptieren. Jedes Speicher format verfügt über eine entsprechende Klasse, die Speicher optionen für dieses Speicher format enthält.
---
##  **3D Optionen zum Speichern von Dateien**
Es gibt mehrere [`Scene.save`](https://reference.aspose.com/3d/net/aspose.threed/scene)-Methoden überlastungen, die ein `SaveOptions`-Objekt akzeptieren. Dies sollte ein Objekt einer Klasse sein, die von der `SaveOptions`-Klasse abgeleitet ist. Jedes Speicher format verfügt über eine entsprechende Klasse, die Speicher optionen für dieses Speicher format enthält. Beispiels weise gibt es `ColladaSaveOptions` für das `FileFormat.Collada`-Speicher format.
###  **Verwendung der Collada Speicher optionen**
Der folgende Code zeigt, wie Sie Speicher optionen festlegen, bevor Sie eine 3D-Datei im Collada-Format speichern.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-ColladaSaveOption.py" >}}
###  **Verwendung der Discreet3DS Speicher optionen**
Der folgende Code zeigt, wie Sie Speicher optionen festlegen, bevor Sie eine 3D-Datei in ein diskretes 3DS-Format speichern.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-Discreet3DSSaveOption.py" >}}
###  **Verwendung der FBX Speicher optionen**
Der folgende Code zeigt, wie Sie Speicher optionen festlegen, bevor Sie eine 3D-Datei in ein FBX-Format speichern.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-FBXSaveOption.py" >}}

`FBXSaveOptions` legt auch die Eigenschaft `enable_compression` bereit, mit der große Binär daten in der FBX-Datei komprimiert werden können. Der Standardwert dieser Eigenschaft ist wahr. Unter dem Code-Snippet wird erläutert, wie Sie mit dieser Eigenschaft arbeiten können, während Sie eine Szene speichern.



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-Save3DScene-Compression.py" >}}
###  **Verwendung der Obj Save-Optionen**
Der folgende Code zeigt, wie Sie Speicher optionen festlegen, bevor Sie eine 3D-Datei in ein Obj-Format speichern.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-ObjSaveOption.py" >}}
###  **Verwendung der STL Speicher optionen**
Der folgende Code zeigt, wie Sie Speicher optionen festlegen, bevor Sie eine 3D-Datei im STL-Format speichern.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-STLSaveOption.py" >}}
###  **Verwendung der U3D Speicher optionen**
Der folgende Code zeigt, wie Sie Speicher optionen festlegen, bevor Sie ein Dokument im U3D-Format speichern.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-U3DSaveOption.py" >}}
###  **Verwendung der glTF Speicher optionen**
{{% alert color="primary" %}} 

Diese Funktion wird von Version 19.8 oder höher unterstützt.

{{% /alert %}} 



Der folgende Code zeigt, wie Sie Speicher optionen festlegen, bevor Sie ein Dokument im glTF-Format speichern.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-glTFSaveOptions.py" >}}
###  **Pretty Print in glTF Speicher optionen**
Sie können auch die Pretty Print-Eigenschaft der GLTF SaveOptions-Klasse für den vom Menschen verständlichen JSON-Druck verwenden. Der folgende Code zeigt, wie diese Funktional ität verwendet wird.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-PrettyPrintInGltfSaveOption.py" >}}
###  **Speichern von Abhängigkeiten einer 3D-Szene im realen Dateisystem**
Entwickler müssen möglicher weise alle 3D Szenen abhängigkeiten im realen Dateisystem speichern. Sie können den Pfad eines lokalen Verzeichnisses definieren, im MemoryFileSystem-Objekt speichern oder Abhängigkeiten einfach verwerfen. Die FileSystem-Eigenschaft wird in den Klassen für alle Speicher optionen hinzugefügt.
####  **Speichern der Material dateien verwerfen**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-DiscardSavingMaterial.py" >}}
####  **Abhängigkeiten im lokalen Verzeichnis speichern**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-SavingDependenciesInLocalDirectory.py" >}}
####  **Abhängigkeiten im MemoryFileSystem-Objekt speichern**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-SavingDependenciesInMemoryFileSystem.py" >}}
###  **Verwendung der Optionen für das Speichern von Google Draco (.drc)**
Der folgende Code zeigt, wie Sie Speicher optionen festlegen, bevor Sie ein 3D-Modell im DRC-Format speichern.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-DRCSaveOptions.py" >}}
###  **Verwendung der RVM Speicher optionen**
Der folgende Code zeigt, wie Sie Speicher optionen festlegen, bevor Sie ein 3D-Modell im RVM-Format speichern.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-RVMSaveOptions.py" >}}
