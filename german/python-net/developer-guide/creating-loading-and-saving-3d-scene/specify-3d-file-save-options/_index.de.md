---
title: Wählen Sie 3D Optionen zum Speichern von Dateien
type: docs
weight: 40
url: /de/python-net/specify-3d-file-save-options/
description: Es gibt mehrere Scene.Save-Methoden überladungen, die ein SaveOptions-Objekt akzeptieren. Jedes Speicher format verfügt über eine entsprechende Klasse, die Speicher optionen für dieses Speicher format enthält.
---
## **3D Optionen zum Speichern von Dateien**
Es gibt mehrere Überlastungen der Methode [`Scene.save`](https://reference.aspose.com/3d/net/aspose.threed/scene), die ein Objekt `SaveOptions` akzeptieren. Dies sollte ein Objekt einer Klasse sein, die aus der Klasse `SaveOptions` abgeleitet ist. Jedes Speicher format verfügt über eine entsprechende Klasse, die Speicher optionen für dieses Speicher format enthält. Beispiels weise gibt es `ColladaSaveOptions` für das Speicher format `FileFormat.Collada`.
### **Verwendung der Speicher optionen Collada**
Der folgende Code zeigt, wie Sie Speicher optionen festlegen, bevor Sie eine 3D-Datei im Format Collada speichern.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-ColladaSaveOption.py" >}}
### **Verwendung der Speicher optionen Discreet3DS**
Der folgende Code zeigt, wie Sie Speicher optionen festlegen, bevor Sie eine 3D-Datei in ein diskretes 3DS-Format speichern.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-Discreet3DSSaveOption.py" >}}
### **Verwendung der Speicher optionen FBX**
Der folgende Code zeigt, wie Sie Speicher optionen festlegen, bevor Sie eine 3D-Datei im Format FBX speichern.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-FBXSaveOption.py" >}}

`FBXSaveOptions` enthüllt auch die Eigenschaft `enable_compression`, die verwendet werden kann, um große binäre Daten in der Datei FBX zu komprimieren. Der Standardwert dieser Eigenschaft ist wahr. Unter dem Code-Snippet wird erläutert, wie Sie mit dieser Eigenschaft arbeiten können, während Sie eine Szene speichern.



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-Save3DScene-Compression.py" >}}
### **Verwendung der Obj Save-Optionen**
Der folgende Code zeigt, wie Sie Speicher optionen festlegen, bevor Sie eine 3D-Datei in ein Obj-Format speichern.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-ObjSaveOption.py" >}}
### **Verwendung der Speicher optionen STL**
Der folgende Code zeigt, wie Sie Speicher optionen festlegen, bevor Sie eine 3D-Datei im Format STL speichern.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-STLSaveOption.py" >}}
### **Verwendung der Speicher optionen U3D**
Der folgende Code zeigt, wie Sie Speicher optionen festlegen, bevor Sie ein Dokument im Format U3D speichern.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-U3DSaveOption.py" >}}
### **Verwendung der Speicher optionen glTF**
{{% alert color="primary" %}} 

Diese Funktion wird von Version 19.8 oder höher unterstützt.

{{% /alert %}} 



Der folgende Code zeigt, wie Sie Speicher optionen festlegen, bevor Sie ein Dokument im Format glTF speichern.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-glTFSaveOptions.py" >}}
### **Pretty Print in glTF Optionen speichern**
Sie können auch die Pretty Print-Eigenschaft der GLTF SaveOptions-Klasse für den vom Menschen verständlichen JSON-Druck verwenden. Der folgende Code zeigt, wie diese Funktional ität verwendet wird.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-PrettyPrintInGltfSaveOption.py" >}}
### **Speichern Sie Abhängigkeiten einer 3D Szene im realen Dateisystem**
Entwickler müssen möglicher weise alle Szenen abhängigkeiten 3D im realen Dateisystem speichern. Sie können den Pfad eines lokalen Verzeichnisses definieren, im MemoryFileSystem-Objekt speichern oder Abhängigkeiten einfach verwerfen. Die FileSystem-Eigenschaft wird in den Klassen für alle Speicher optionen hinzugefügt.
#### **Speichern der Material dateien verwerfen**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-DiscardSavingMaterial.py" >}}
#### **Abhängigkeiten im lokalen Verzeichnis speichern**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-SavingDependenciesInLocalDirectory.py" >}}
#### **Abhängigkeiten im MemoryFileSystem-Objekt speichern**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-SavingDependenciesInMemoryFileSystem.py" >}}
### **Verwendung der Google Draco (.drc) Speicher optionen**
Der folgende Code zeigt, wie Sie Speicher optionen festlegen, bevor Sie ein Modell 3D im Format DRC speichern.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-DRCSaveOptions.py" >}}
### **Verwendung der Speicher optionen RVM**
Der folgende Code zeigt, wie Sie Speicher optionen festlegen, bevor Sie ein Modell 3D im Format RVM speichern.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-RVMSaveOptions.py" >}}
