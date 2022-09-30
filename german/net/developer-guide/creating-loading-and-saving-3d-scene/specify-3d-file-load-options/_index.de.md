---
title: Geben Sie 3D Datei lade optionen in C# an
linktitle: Geben Sie 3D Datei lade optionen an
type: docs
weight: 30
url: /de/net/specify-3d-file-load-options/
description: Es gibt mehrere Scene.Open-Methode überlastet oder Scene-Class-Konstruktor-Überladungen, die ein Load Options-Objekt akzeptieren. Jedes Last format verfügt über eine entsprechende Klasse, die Last optionen für dieses Last format enthält.
---
## **Übersicht**

Dieser Artikel erklärt, wie Sie verschiedene Arten von 3D-Dateien mit ihren jeweiligen Load-Option-Klassen in C# innerhalb des Scene-Objekts laden können und dann können Sie[Speichern Sie es in verschiedenen unterstützten Dateiformaten 3D](https://docs.aspose.com/3d/net/specify-3d-file-save-options/). Durch Laden und Speichern können Sie eine Anzahl verschiedener Konvertie rungen durchführen, z.

- C# FBX auf OBJ umrechnen
- C# 3DS auf FBX umrechnen
- C# U3D auf OBJ umrechnen
- C# OBJ auf 3DS umrechnen
- X an 3DS in C# umwandeln

## **3D Datei lade optionen**
Es gibt mehrere Überladungen von [`Scene.Open`](https://reference.aspose.com/3d/net/aspose.threed/scene) Methoden oder Überlastungen von Scene-Klassen konstruktoren, die ein `LoadOptions`-Objekt akzeptieren. Dies sollte ein Objekt einer Klasse sein, die aus der Klasse `LoadOptions` abgeleitet ist. Jedes Lade format verfügt über eine entsprechende Klasse, die Last optionen für dieses Last format enthält. Beispiels weise gibt es `ColladaSaveOptions` für das Speicher format `FileFormat.Collada`.
### **Verwendung der diskreten Lade optionen 3DS**
Der unten stehende Code C# zeigt, wie Sie Lade optionen festlegen, bevor Sie eine Discreet 3DS-Datei laden.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-Discreet3DSOption.cs" >}}
### **Verwendung der Obj-Lade optionen**
Der unten stehende Code C# zeigt, wie Sie Lade optionen festlegen, bevor Sie eine Obj-Datei 3D laden.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-ObjLoadOption.cs" >}}
### **Nutzung der Lade optionen STL**
Der unten stehende Code C# zeigt, wie Sie Lade optionen festlegen, bevor Sie eine STL-Datei laden.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-STLLoadOption.cs" >}}
### **Nutzung der Lade optionen U3D**
Der unten stehende Code C# zeigt, wie Sie Lade optionen festlegen, bevor Sie eine U3D-Datei laden.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-U3DLoadOption.cs" >}}
### **Nutzung der Lade optionen glTF**
Der unten stehende Code C# zeigt, wie Sie Lade optionen festlegen, bevor Sie eine glTF-Datei laden.
#### **Drehen Sie die V/T-Textur koordination um**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-glTFLoadOptions.cs" >}}
### **Verwendung der Ply-Load-Optionen**
Der folgende Code C# zeigt, wie Sie Lade optionen festlegen, bevor Sie ein PLY-Modell laden.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-PlyLoadOptions.cs" >}}
### **Nutzung der Lade optionen DirectX X**
Der unten stehende Code C# zeigt, wie Sie Lade optionen festlegen, bevor Sie eine DirectX X-Datei laden.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-XLoadOptions.cs" >}}
### **Lade optionen RVM nutzen**
**C#**

{{< highlight "java" >}}

 // set load options of RVM

Scene scene = new Scene();

var opt = new RvmLoadOptions()

{

    CylinderRadialSegments = 32,

    DishLatitudeSegments = 16,

    DishLongitudeSegments = 24,

    TorusTubularSegments = 40

};

// import RVM

scene.Open("LAD-TOP.rvm", opt);

// save in the OBJ format

scene.Save("LAD-TOP.obj", FileFormat.WavefrontOBJ);

{{< /highlight >}}
### **Verwendung von FBX Lade optionen**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-FBXLoadOptions.cs" >}}
