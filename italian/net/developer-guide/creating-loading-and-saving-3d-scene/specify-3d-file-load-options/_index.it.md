---
title: Specificare 3D Opzioni di caricamento file in C#
linktitle: Specificare 3D Opzioni di caricamento file
type: docs
weight: 30
url: /it/net/specify-3d-file-load-options/
description: Esistono diversi overload del metodo Scene.Open o overload del costruttore di classi Scene che accettano un oggetto LoadOptions. Ogni formato di carico ha una classe corrispondente che contiene le opzioni di carico per quel formato di carico.
---
##  **Panoramica**

Questo articolo spiega come è possibile caricare diversi tipi di file 3D utilizzando le rispettive classi di opzioni di carico in C# all'interno dell'oggetto Scena e quindi è possibile [Salvarlo in diversi formati di file supportati da 3D](https://docs.aspose.com/3d/net/specify-3d-file-save-options/). Caricando e salvando, puoi eseguire il numero di conversioni diverse, ad es.

- Convertire FBX in OBJ in C#
- Convertire 3DS in FBX in C#
- Convertire U3D in OBJ in C#
- Convertire OBJ in 3DS in C#
- Converti da X a 3DS in C#

##  **3D Opzioni di caricamento file**
Sono disponibili diversi overload del metodo [`Scene.Open`](https://reference.aspose.com/3d/net/aspose.threed/scene) o overload del costruttore di classi Scene che accettano un oggetto `LoadOptions`. Questo dovrebbe essere un oggetto di una classe derivata dalla classe `LoadOptions`. Ogni formato di carico ha una classe corrispondente che contiene le opzioni di carico per quel formato di carico, ad esempio c' è `ColladaSaveOptions` per il formato di salvataggio `FileFormat.Collada`.
###  **Utilizzo delle opzioni di carico discre 3DS**
Il codice C# di seguito mostra come impostare le opzioni di carico prima di caricare un file Discreet 3DS.

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
###  **Utilizzo delle opzioni di carico Obj**
Il codice C# di seguito mostra come impostare le opzioni di carico prima di caricare un file Obj 3D.

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
###  **Utilizzo delle opzioni di carico STL**
Il codice C# di seguito mostra come impostare le opzioni di carico prima di caricare un file STL.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize an object
StlLoadOptions loadSTLOpts = new StlLoadOptions();
// Flip the coordinate system.
loadSTLOpts.FlipCoordinateSystem = true;
// Configure the look up paths to allow importer to find external dependencies.
loadSTLOpts.LookupPaths = new List<string>(new string[] { "textures" });

{{< /highlight >}}
###  **Utilizzo delle opzioni di carico U3D**
Il codice C# di seguito mostra come impostare le opzioni di carico prima di caricare un file U3D.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize an object
U3dLoadOptions loadU3DOpts = new U3dLoadOptions();
// Flip the coordinate system.
loadU3DOpts.FlipCoordinateSystem = true;
// Configure the look up paths to allow importer to find external dependencies.
loadU3DOpts.LookupPaths = new List<string>(new string[] { "textures" });

{{< /highlight >}}
###  **Utilizzo delle opzioni di carico glTF**
Il codice C# di seguito mostra come impostare le opzioni di carico prima di caricare un file glTF.
####  **Capovolgi la Coordinata texture V/T**
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
###  **Utilizzo delle opzioni di carico Ply**
Il codice C# di seguito mostra come impostare le opzioni di carico prima di caricare un modello PLY.

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
###  **Utilizzo delle opzioni di carico DirectX X**
Il codice C# di seguito mostra come impostare le opzioni di carico prima di caricare un file DirectX X.

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
###  **Utilizza RVM opzioni di carico**
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
###  **Utilizzo di FBX opzioni di carico**
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
