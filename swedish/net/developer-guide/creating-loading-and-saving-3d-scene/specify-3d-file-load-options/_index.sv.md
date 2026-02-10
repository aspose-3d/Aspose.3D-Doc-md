---
title: Ange 3D Ladda alternativ för fil i C#
linktitle: Ange 3D Ladda alternativ för filName
type: docs
weight: 30
url: /sv/net/specify-3d-file-load-options/
description: Det finns flera Scene.Öppen metod överbelastning eller Scene klass konstruktor överbelastning som accepterar ett LoadOptions objekt. Varje lastformat har en motsvarande klass som innehåller belastningsalternativ för det belastningsformatet.
---
##  **Översikt**

Den här artikeln förklarar hur du kan ladda olika typer av 3D genom att använda deras respektive laddningsalternativ klasser i C# Scene-objektet och sedan kan du [Spara den i olika 3D som stöds](https://docs.aspose.com/3d/net/specify-3d-file-save-options/). Genom att ladda och spara kan du utföra antal olika konverteringar, t.ex.

- Konvertera FBX till OBJ i C#
- Konvertera 3DS till FBX i C#
- Konvertera U3D till OBJ i C#
- Konvertera OBJ till 3DS i C#
- Konvertera X till 3DS i C#

##  **3D Ladda ner filer**
Det finns flera överbelastningar av [`Scene.Open`](https://reference.aspose.com/3d/net/aspose.threed/scene) metoden eller överbelastningar av konstruktörsklass som accepterar ett `LoadOptions`-objekt. Detta bör vara ett föremål för en klass som härrör från klassen `LoadOptions`. Varje belastningsformat har en motsvarande klass som innehåller belastningsalternativ för det belastningsformatet. till exempel finns `ColladaSaveOptions` för `FileFormat.Collada` spara formatet.
###  **Use of the Discreet 3DS Load Options**
C#-koden nedan visar hur laddningsalternativ ska ställas innan en Diskret 3DS-fil lads.

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
###  **Användning av Obj-lastalternativ**
C#-koden nedan visar hur laddningsalternativ ska ställas innan en 3D Obj-fil laddas.

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
###  **Användning av laddandealternativ för STLName**
C#-koden nedan visar hur laddningsalternativ ska ställas innan en STL-fil lads.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize an object
StlLoadOptions loadSTLOpts = new StlLoadOptions();
// Flip the coordinate system.
loadSTLOpts.FlipCoordinateSystem = true;
// Configure the look up paths to allow importer to find external dependencies.
loadSTLOpts.LookupPaths = new List<string>(new string[] { "textures" });

{{< /highlight >}}
###  **Användning av laddandealternativ för U3DName**
C#-koden nedan visar hur laddningsalternativ ska ställas innan en U3D-fil laddas.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize an object
U3dLoadOptions loadU3DOpts = new U3dLoadOptions();
// Flip the coordinate system.
loadU3DOpts.FlipCoordinateSystem = true;
// Configure the look up paths to allow importer to find external dependencies.
loadU3DOpts.LookupPaths = new List<string>(new string[] { "textures" });

{{< /highlight >}}
###  **Användning av laddandealternativ för glTFName**
C#-koden nedan visar hur laddningsalternativ ska ställas innan en glTF-fil laddas.
####  **Vänd V/T texturkoordinat**
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
###  **Användning av Ply-lastalternativ**
C#-koden nedan visar hur laddningsalternativ ska ställas innan en PLY-modell lads.

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
###  **Användning av DirectX X-lastalternativ**
C#-koden nedan visar hur laddningsalternativ ska ställas innan en DirectX-fil laddas.

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
###  **Use RVM load options**
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
###  **Using FBX Load Options**
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
