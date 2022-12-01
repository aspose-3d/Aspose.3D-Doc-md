---
title: Geben Sie 3D Datei speichern Optionen in C# an
linktitle: Wählen Sie 3D Optionen zum Speichern von Dateien
type: docs
weight: 40
url: /de/net/specify-3d-file-save-options/
description: Es gibt mehrere Scene.Save-Methoden überladungen, die ein SaveOptions-Objekt akzeptieren. Jedes Speicher format verfügt über eine entsprechende Klasse, die Speicher optionen für dieses Speicher format enthält.
---
## **Übersicht**

Dieser Artikel erklärt, wie Sie 3D-Dateien in verschiedenen Formaten speichern können[Nach dem Laden in Szene Objekt](https://docs.aspose.com/3d/net/specify-3d-file-load-options/)Unter Verwendung von C#. Durch Laden und Speichern können Sie eine Anzahl verschiedener Konvertie rungen durchführen, z.

- FBX zu X konvertieren in C#
- C# GLTF auf OBJ umrechnen
- OBJ zu X konvertieren in C#
- C# STL auf OBJ umrechnen
- C# RVM auf 3DS umrechnen

## **3D Optionen zum Speichern von Dateien**
Es gibt mehrere Überladungen von [`Scene.Save`](https://reference.aspose.com/3d/net/aspose.threed/scene) Methoden, die ein SaveOptions-Objekt akzeptieren. Dies sollte ein Objekt einer Klasse sein, die von der Klasse `SaveOptions` abgeleitet ist. Jedes Speicher format verfügt über eine entsprechende Klasse, die Speicher optionen für dieses Speicher format enthält. Beispiels weise gibt es `ColladaSaveOptions` für das Speicher format `FileFormat.Collada`.
### **Verwendung der Speicher optionen Collada**
Der unten stehende Code C# zeigt, wie Sie Speicher optionen festlegen, bevor Sie eine 3D-Datei im Format Collada speichern.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-ColladaSaveOption.cs" >}}
### **Verwendung der Speicher optionen Discreet3DS**
Der unten stehende C#-Code zeigt, wie Sie Speicher optionen festlegen, bevor Sie eine 3D-Datei in ein diskretes 3DS-Format speichern.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-Discreet3DSSaveOption.cs" >}}
### **Verwendung der Speicher optionen FBX**
Der unten stehende Code C# zeigt, wie Sie Speicher optionen festlegen, bevor Sie eine Datei 3D in ein Format FBX speichern.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-FBXSaveOption.cs" >}}

`FBXSaveOptions` enthüllt auch die Eigenschaft `EnableCompression`, die verwendet werden kann, um große binäre Daten in der Datei FBX zu komprimieren. Der Standardwert dieser Eigenschaft ist wahr. Unter dem Code-Snippet wird erläutert, wie Sie mit dieser Eigenschaft arbeiten können, während Sie eine Szene speichern.



{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-Save3DScene-Compression.cs" >}}
### **Verwendung der Obj Save-Optionen**
Der folgende Code zeigt, wie Sie Speicher optionen festlegen, bevor Sie eine 3D-Datei in ein Obj-Format speichern.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-ObjSaveOption.cs" >}}
### **Verwendung der Speicher optionen STL**
Der unten stehende Code C# zeigt, wie Sie Speicher optionen festlegen, bevor Sie eine 3D-Datei im Format STL speichern.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-STLSaveOption.cs" >}}
### **Verwendung der Speicher optionen U3D**
Der unten stehende Code C# zeigt, wie Sie Speicher optionen festlegen, bevor Sie ein Dokument im Format U3D speichern.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-U3DSaveOption.cs" >}}
### **Verwendung der Speicher optionen glTF**
{{% alert color="primary" %}} 

Diese Funktion wird von Version 19.8 oder höher unterstützt.

{{% /alert %}} 



Der unten stehende Code C# zeigt, wie Sie Speicher optionen festlegen, bevor Sie ein Dokument im Format glTF speichern.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-glTFSaveOptions.cs" >}}
### **Pretty Print in glTF Optionen speichern**
Sie können auch die Pretty Print-Eigenschaft der GLTF SaveOptions-Klasse für den vom Menschen verständlichen JSON-Druck verwenden. Der folgende Code zeigt, wie diese Funktional ität verwendet wird.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-PrettyPrintInGltfSaveOption.cs" >}}
### **Speichern Sie Abhängigkeiten einer 3D Szene im realen Dateisystem**
Entwickler müssen möglicher weise alle Szenen abhängigkeiten 3D im realen Dateisystem speichern. Sie können den Pfad eines lokalen Verzeichnisses definieren, im Objekt `MemoryFileSystem` speichern oder Abhängigkeiten einfach verwerfen. Die Eigenschaft `FileSystem` wird in den Klassen für alle Optionen zum Speichern hinzugefügt.
#### **Speichern der Material dateien verwerfen**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-DiscardSavingMaterial.cs" >}}
#### **Abhängigkeiten im lokalen Verzeichnis speichern**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-SavingDependenciesInLocalDirectory.cs" >}}
#### **Abhängigkeiten im MemoryFileSystem-Objekt speichern**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-SavingDependenciesInMemoryFileSystem.cs" >}}
### **Verwendung der Google Draco (.drc) Speicher optionen**
Der folgende Code C# zeigt, wie Sie Speicher optionen festlegen, bevor Sie ein 3D-Modell im Format DRC speichern.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-DRCSaveOptions.cs" >}}
### **Verwendung der Speicher optionen RVM**
Der folgende Code C# zeigt, wie Sie Speicher optionen festlegen, bevor Sie ein 3D-Modell im Format RVM speichern.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-RVMSaveOptions.cs" >}}
