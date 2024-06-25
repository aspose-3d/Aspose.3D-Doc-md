---
title: Geben Sie 3D Datei lade optionen in C# an
linktitle: 3D Datei lade optionen angeben
type: docs
weight: 30
url: /de/net/specify-3d-file-load-options/
description: Es gibt mehrere Scene.Open-Methode überlastet oder Scene-Class-Konstruktor-Überladungen, die ein Load Options-Objekt akzeptieren. Jedes Last format verfügt über eine entsprechende Klasse, die Last optionen für dieses Last format enthält.
---
##  **Übersicht**

In diesem Artikel wird erläutert, wie Sie verschiedene Arten von 3D-Dateien mit ihren jeweiligen Load-Options klassen in C# innerhalb des Scene-Objekts laden können und dann [Speichern Sie es in verschiedenen 3D unterstützten Dateiformaten](https://docs.aspose.com/3d/net/specify-3d-file-save-options/). Durch Laden und Speichern können Sie eine Anzahl verschiedener Konvertie rungen durchführen, z.

- FBX zu OBJ in C# umrechnen
- 3DS zu FBX in C# umrechnen
- U3D zu OBJ in C# umrechnen
- OBJ zu 3DS in C# umrechnen
- X zu 3DS in C# konvertieren

##  **3D Datei lade optionen**
Es gibt mehrere Überladungen von [`Scene.Open`](https://reference.aspose.com/3d/net/aspose.threed/scene)-Methoden oder Überladungen von Scene-Klassen konstruktoren, die ein `LoadOptions`-Objekt akzeptieren. Dies sollte ein Objekt einer Klasse sein, die von der `LoadOptions`-Klasse abgeleitet ist. Jedes Lade format verfügt über eine entsprechende Klasse, die Lade optionen für dieses Last format enthält. Beispiels weise gibt es `ColladaSaveOptions` für das `FileFormat.Collada`-Speicher format.
###  **Verwendung der diskreten 3DS-Lade optionen**
Der unten stehende C#-Code zeigt, wie Sie Lade optionen festlegen, bevor Sie eine Diskrete 3DS-Datei laden.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-Discreet3DSOption.cs" >}}
###  **Verwendung der Obj-Lade optionen**
Der unten stehende C#-Code zeigt, wie Sie Lade optionen festlegen, bevor Sie eine 3D Obj-Datei laden.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-ObjLoadOption.cs" >}}
###  **Verwendung der STL-Lade optionen**
Der unten stehende C#-Code zeigt, wie Sie Lade optionen festlegen, bevor Sie eine STL-Datei laden.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-STLLoadOption.cs" >}}
###  **Verwendung der U3D-Lade optionen**
Der unten stehende C#-Code zeigt, wie Sie Lade optionen festlegen, bevor Sie eine U3D-Datei laden.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-U3DLoadOption.cs" >}}
###  **Verwendung der glTF-Lade optionen**
Der unten stehende C#-Code zeigt, wie Sie Lade optionen festlegen, bevor Sie eine glTF-Datei laden.
####  **Drehen Sie die V/T-Textur koordination um**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-glTFLoadOptions.cs" >}}
###  **Verwendung der Ply-Load-Optionen**
Der unten stehende C#-Code zeigt, wie Sie Lade optionen festlegen, bevor Sie ein PLY-Modell laden.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-PlyLoadOptions.cs" >}}
###  **Verwendung der DirectX X-Lade optionen**
Der unten stehende C#-Code zeigt, wie Sie Lade optionen festlegen, bevor Sie eine DirectX X-Datei laden.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-XLoadOptions.cs" >}}
###  **Verwenden Sie die Lade optionen für RVM**
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
###  **Verwendung von FBX Lade optionen**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-FBXLoadOptions.cs" >}}
