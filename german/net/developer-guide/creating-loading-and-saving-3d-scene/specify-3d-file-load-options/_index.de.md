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

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
Discreet3dsLoadOptions loadOpts = new Discreet3dsLoadOptions();
// Sets wheather to use the transformation defined in the first frame of animation track.
loadOpts.ApplyAnimationTransform = true;
// Flip the coordinate system
loadOpts.FlipCoordinateSystem = true;
// Prefer to use gamma-corrected color if a 3ds file provides both original color and gamma-corrected color.
loadOpts.GammaCorrectedColor = true;
// Configure the look up paths to allow importer to find external dependencies.
loadOpts.LookupPaths = new List<string>(new string[] { "textures" });

{{< /highlight >}}
###  **Verwendung der Obj-Lade optionen**
Der unten stehende C#-Code zeigt, wie Sie Lade optionen festlegen, bevor Sie eine 3D Obj-Datei laden.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize an object
ObjLoadOptions loadObjOpts = new ObjLoadOptions();
// Import materials from external material library file
loadObjOpts.EnableMaterials = true;
// Flip the coordinate system.
loadObjOpts.FlipCoordinateSystem = true;
// Configure the look up paths to allow importer to find external dependencies.
loadObjOpts.LookupPaths.Add("textures");

{{< /highlight >}}
###  **Verwendung der STL-Lade optionen**
Der unten stehende C#-Code zeigt, wie Sie Lade optionen festlegen, bevor Sie eine STL-Datei laden.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize an object
StlLoadOptions loadSTLOpts = new StlLoadOptions();
// Flip the coordinate system.
loadSTLOpts.FlipCoordinateSystem = true;
// Configure the look up paths to allow importer to find external dependencies.
loadSTLOpts.LookupPaths = new List<string>(new string[] { "textures" });

{{< /highlight >}}
###  **Verwendung der U3D-Lade optionen**
Der unten stehende C#-Code zeigt, wie Sie Lade optionen festlegen, bevor Sie eine U3D-Datei laden.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize an object
U3dLoadOptions loadU3DOpts = new U3dLoadOptions();
// Flip the coordinate system.
loadU3DOpts.FlipCoordinateSystem = true;
// Configure the look up paths to allow importer to find external dependencies.
loadU3DOpts.LookupPaths = new List<string>(new string[] { "textures" });

{{< /highlight >}}
###  **Verwendung der glTF-Lade optionen**
Der unten stehende C#-Code zeigt, wie Sie Lade optionen festlegen, bevor Sie eine glTF-Datei laden.
####  **Drehen Sie die V/T-Textur koordination um**
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize Scene class object
Scene scene = new Scene();
// Set load options
GltfLoadOptions loadOpt = new GltfLoadOptions();
// The default value is true, usually we don't need to change it. Aspose.3D will automatically flip the V/T texture coordinate during load and save.       
loadOpt.FlipTexCoordV = true;
scene.Open("Duck.gltf", loadOpt);

{{< /highlight >}}
###  **Verwendung der Ply-Load-Optionen**
Der unten stehende C#-Code zeigt, wie Sie Lade optionen festlegen, bevor Sie ein PLY-Modell laden.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// initialize Scene class object
Scene scene = new Scene();
// initialize an object
PlyLoadOptions loadPLYOpts = new PlyLoadOptions();
// Flip the coordinate system.
loadPLYOpts.FlipCoordinateSystem = true;
// load 3D Ply model
scene.Open("vase-v2.ply", loadPLYOpts);

{{< /highlight >}}
###  **Verwendung der DirectX X-Lade optionen**
Der unten stehende C#-Code zeigt, wie Sie Lade optionen festlegen, bevor Sie eine DirectX X-Datei laden.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// initialize Scene class object
Scene scene = new Scene();
// initialize an object
XLoadOptions loadXOpts = new XLoadOptions(FileContentType.ASCII);
// flip the coordinate system.
loadXOpts.FlipCoordinateSystem = true;
// load 3D X file
scene.Open("warrior.x", loadXOpts);

{{< /highlight >}}
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
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
//This will output all properties defined in GlobalSettings in FBX file.
Scene scene = new Scene();
var opt = new FbxLoadOptions() { KeepBuiltinGlobalSettings = true };
scene.Open("test.FBX", opt);
foreach (Property property in scene.RootNode.AssetInfo.Properties)
{
    Console.WriteLine(property);
}

{{< /highlight >}}
