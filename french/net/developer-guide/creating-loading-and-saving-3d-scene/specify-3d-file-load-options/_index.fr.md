---
title: Spécifiez 3D Options de chargement de fichier dans C#
linktitle: Spécifiez 3D Options de chargement de fichier
type: docs
weight: 30
url: /fr/net/specify-3d-file-load-options/
description: Il existe plusieurs surcharges de méthode Scene.Open ou surcharges de constructeur de classe Scène qui acceptent un objet LoadOptions. Chaque format de charge a une classe correspondante qui contient les options de charge pour ce format de charge.
---
##  **Aperçu**

Cet article explique comment vous pouvez charger différents types de fichiers 3D en utilisant leurs classes d'option de chargement respectives dans C# à l'intérieur de l'objet Scène, puis vous pouvez [Enregistrez-le dans différents formats de fichiers supportés par 3D](https://docs.aspose.com/3d/net/specify-3d-file-save-options/). En chargeant et en sauvegardant, vous pouvez effectuer un nombre de conversions différentes, par ex.

- Convertir FBX en OBJ en C#
- Convertir 3DS en FBX en C#
- Convertir U3D en OBJ en C#
- Convertir OBJ en 3DS en C#
- Convertir X en 3DS en C#

##  **3D Options de chargement des fichiers**
Il existe plusieurs surcharges de méthode [`Scene.Open`](https://reference.aspose.com/3d/net/aspose.threed/scene) ou surcharges de constructeur de classe Scene qui acceptent un objet `LoadOptions`. Cela devrait être un objet d'une classe dérivée de la classe `LoadOptions`. Chaque format de chargement a une classe correspondante qui contient des options de chargement pour ce format de chargement, par exemple il y a `ColladaSaveOptions` pour le format de sauvegarde `FileFormat.Collada`.
###  **Utilisation des options de chargement de 3DS discret**
Le code C# ci-dessous montre comment définir les options de chargement avant de charger un fichier Discreet 3DS.

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
###  **Utilisation des options de charge Obj**
Le code C# ci-dessous montre comment définir les options de chargement avant de charger un fichier 3D Obj.

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
###  **Utilisation des options de chargement STL**
Le code C# ci-dessous montre comment définir les options de chargement avant de charger un fichier STL.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize an object
StlLoadOptions loadSTLOpts = new StlLoadOptions();
// Flip the coordinate system.
loadSTLOpts.FlipCoordinateSystem = true;
// Configure the look up paths to allow importer to find external dependencies.
loadSTLOpts.LookupPaths = new List<string>(new string[] { "textures" });

{{< /highlight >}}
###  **Utilisation des options de chargement U3D**
Le code C# ci-dessous montre comment définir les options de chargement avant de charger un fichier U3D.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize an object
U3dLoadOptions loadU3DOpts = new U3dLoadOptions();
// Flip the coordinate system.
loadU3DOpts.FlipCoordinateSystem = true;
// Configure the look up paths to allow importer to find external dependencies.
loadU3DOpts.LookupPaths = new List<string>(new string[] { "textures" });

{{< /highlight >}}
###  **Utilisation des options de chargement glTF**
Le code C# ci-dessous montre comment définir les options de chargement avant de charger un fichier glTF.
####  **Retournez la coordination de la texture V/T**
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
###  **Utilisation des options de charge Ply**
Le code C# ci-dessous montre comment définir les options de chargement avant de charger un modèle PLY.

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
###  **Utilisation des options de charge DirectX X**
Le code C# ci-dessous montre comment définir les options de chargement avant de charger un fichier DirectX X.

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
###  **Utiliser les options de chargement RVM**
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
###  **Utilisation des options de chargement FBX**
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
