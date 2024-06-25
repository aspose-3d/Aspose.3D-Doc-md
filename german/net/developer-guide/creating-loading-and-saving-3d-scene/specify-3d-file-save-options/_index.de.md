---
title: Geben Sie 3D Optionen zum Speichern von Dateien in C# an
linktitle: 3D Optionen zum Speichern von Dateien angeben
type: docs
weight: 40
url: /de/net/specify-3d-file-save-options/
description: Es gibt mehrere Scene.Save-Methoden überladungen, die ein SaveOptions-Objekt akzeptieren. Jedes Speicher format verfügt über eine entsprechende Klasse, die Speicher optionen für dieses Speicher format enthält.
---
##  **Übersicht**

Dieser Artikel erklärt, wie Sie 3D-Dateien in verschiedenen Formaten [Nach dem Laden in Szene Objekt](https://docs.aspose.com/3d/net/specify-3d-file-load-options/) mit C# speichern können. Durch Laden und Speichern können Sie eine Anzahl verschiedener Konvertie rungen durchführen, z.

- FBX zu X in C# konvertieren
- GLTF zu OBJ in C# umrechnen
- OBJ zu X in C# konvertieren
- STL zu OBJ in C# umrechnen
- RVM zu 3DS in C# umrechnen

##  **3D Optionen zum Speichern von Dateien**
Es gibt mehrere [`Scene.Save`](https://reference.aspose.com/3d/net/aspose.threed/scene)-Methoden überlastungen, die ein SaveOptions-Objekt akzeptieren. Dies sollte ein Objekt einer Klasse sein, die von der `SaveOptions`-Klasse abgeleitet ist. Jedes Speicher format verfügt über eine entsprechende Klasse, die Speicher optionen für dieses Speicher format enthält. Beispiels weise gibt es `ColladaSaveOptions` für das `FileFormat.Collada`-Speicher format.
###  **Verwendung der Collada Speicher optionen**
Der unten stehende C#-Code zeigt, wie Sie Speicher optionen festlegen, bevor Sie eine 3D-Datei im Collada-Format speichern.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-ColladaSaveOption.cs" >}}
###  **Verwendung der Discreet3DS Speicher optionen**
Der unten stehende C#-Code zeigt, wie Sie Speicher optionen festlegen, bevor Sie eine 3D-Datei in ein diskretes 3DS-Format speichern.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-Discreet3DSSaveOption.cs" >}}
###  **Verwendung der FBX Speicher optionen**
Der unten stehende C#-Code zeigt, wie Sie Speicher optionen festlegen, bevor Sie eine 3D-Datei in ein FBX-Format speichern.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-FBXSaveOption.cs" >}}

`FBXSaveOptions` legt auch die Eigenschaft `EnableCompression` bereit, mit der große Binär daten in der FBX-Datei komprimiert werden können. Der Standardwert dieser Eigenschaft ist wahr. Unter dem Code-Snippet wird erläutert, wie Sie mit dieser Eigenschaft arbeiten können, während Sie eine Szene speichern.



{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-Save3DScene-Compression.cs" >}}
###  **Verwendung der Obj Save-Optionen**
Der folgende Code zeigt, wie Sie Speicher optionen festlegen, bevor Sie eine 3D-Datei in ein Obj-Format speichern.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-ObjSaveOption.cs" >}}
###  **Verwendung der STL Speicher optionen**
Der unten stehende C#-Code zeigt, wie Sie Speicher optionen festlegen, bevor Sie eine 3D-Datei im STL-Format speichern.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-STLSaveOption.cs" >}}
###  **Verwendung der U3D Speicher optionen**
Der unten stehende C#-Code zeigt, wie Sie Speicher optionen festlegen, bevor Sie ein Dokument im U3D-Format speichern.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-U3DSaveOption.cs" >}}
###  **Verwendung der glTF Speicher optionen**
{{% alert color="primary" %}} 

Diese Funktion wird von Version 19.8 oder höher unterstützt.

{{% /alert %}} 



Der unten stehende C#-Code zeigt, wie Sie Speicher optionen festlegen, bevor Sie ein Dokument im glTF-Format speichern.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-glTFSaveOptions.cs" >}}
###  **Pretty Print in glTF Speicher optionen**
Sie können auch die Pretty Print-Eigenschaft der GLTF SaveOptions-Klasse für den vom Menschen verständlichen JSON-Druck verwenden. Der folgende Code zeigt, wie diese Funktional ität verwendet wird.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-PrettyPrintInGltfSaveOption.cs" >}}
###  **Speichern von Abhängigkeiten einer 3D-Szene im realen Dateisystem**
Entwickler müssen möglicher weise alle 3D Szenen abhängigkeiten im realen Dateisystem speichern. Sie können den Pfad eines lokalen Verzeichnisses definieren, im `MemoryFileSystem`-Objekt speichern oder einfach Abhängigkeiten verwerfen. Die `FileSystem`-Eigenschaft wird in den All-Save-Options klassen hinzugefügt.
####  **Speichern der Material dateien verwerfen**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-DiscardSavingMaterial.cs" >}}
####  **Abhängigkeiten im lokalen Verzeichnis speichern**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-SavingDependenciesInLocalDirectory.cs" >}}
####  **Abhängigkeiten im MemoryFileSystem-Objekt speichern**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-SavingDependenciesInMemoryFileSystem.cs" >}}
###  **Verwendung der Optionen für das Speichern von Google Draco (.drc)**
Der unten stehende C#-Code zeigt, wie Sie Speicher optionen festlegen, bevor Sie ein 3D-Modell im DRC-Format speichern.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-DRCSaveOptions.cs" >}}
###  **Verwendung der RVM Speicher optionen**
Der unten stehende C#-Code zeigt, wie Sie Speicher optionen festlegen, bevor Sie ein 3D-Modell im RVM-Format speichern.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-RVMSaveOptions.cs" >}}
