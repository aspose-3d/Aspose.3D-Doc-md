---
title: Spécifiez 3D Options de chargement de fichier
type: docs
weight: 10
url: /fr/java/specify-3d-file-load-options/
description: Il existe plusieurs surcharges de méthode Scene.open ou surcharges de constructeur de classe Scène qui acceptent l'instance LoadOptions.
---
##  **3D Options de chargement des fichiers**
Il existe plusieurs surcharges de méthode Scene.open ou surcharges de constructeur de classe Scène qui acceptent l'instance LoadOptions. Il doit s'agir d'une instance d'une classe dérivée de la classe LoadOptions. Chaque format de charge a une classe correspondante qui contient les options de charge pour ce format de charge, par exemple il existe ColladaSaveOptions pour le format de sauvegarde FileFormat.COLLADA.
###  **Utilisation des options de chargement de 3DS discret**
Le code ci-dessous montre comment définir les options de chargement avant de charger un fichier Discreet 3DS.

{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
Discreet3DSLoadOptions loadOpts = new Discreet3DSLoadOptions();
// Sets wheather to use the transformation defined in the first frame of animation track.
loadOpts.setApplyAnimationTransform(true);
// Flip the coordinate system
loadOpts.setFlipCoordinateSystem(true);
// Prefer to use gamma-corrected color if a 3ds file provides both original color and gamma-corrected color.
loadOpts.setGammaCorrectedColor(true);
// Configure the look up paths to allow importer to find external dependencies.
loadOpts.getLookupPaths().add(MyDir);
{{< /highlight >}}
###  **Utilisation des options de charge Obj**
Le code ci-dessous montre comment définir les options de chargement avant de charger un fichier 3D Obj.

{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// Initialize an object
ObjLoadOptions loadObjOpts = new ObjLoadOptions();
// Import materials from external material library file
loadObjOpts.setEnableMaterials(true);
// Flip the coordinate system.
loadObjOpts.setFlipCoordinateSystem(true);
// Configure the look up paths to allow importer to find external dependencies.
loadObjOpts.getLookupPaths().add(MyDir);
{{< /highlight >}}
###  **Utilisation des options de chargement STL**
Le code ci-dessous montre comment définir les options de chargement avant de charger un fichier STL.

{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// Initialize an object
STLLoadOptions loadSTLOpts = new STLLoadOptions();
// Flip the coordinate system.
loadSTLOpts.setFlipCoordinateSystem(true);
// Configure the look up paths to allow importer to find external dependencies.
loadSTLOpts.getLookupPaths().add(MyDir);
{{< /highlight >}}
###  **Utilisation des options de chargement U3D**
Le code ci-dessous montre comment définir les options de chargement avant de charger un fichier U3D.

{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// Initialize an object
U3DLoadOptions loadU3DOpts = new U3DLoadOptions();
// Flip the coordinate system.
loadU3DOpts.setFlipCoordinateSystem(true);
// Configure the look up paths to allow importer to find external dependencies.
loadU3DOpts.getLookupPaths().add(MyDir);
{{< /highlight >}}
###  **Utilisation des options de chargement glTF**
Le code ci-dessous montre comment définir les options de chargement avant de charger un fichier glTF.
####  **Retournez la coordination de la texture V/T**
{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// Initialize Scene class object
Scene scene = new Scene();
// Set load options
GLTFLoadOptions loadOpt = new GLTFLoadOptions();
// The default value is true, usually we don't need to change it. Aspose.3D will automatically flip the V/T texture coordinate during load and save.
loadOpt.setFlipTexCoordV(true);
scene.open( MyDir + "Duck.gltf", loadOpt);
{{< /highlight >}}
###  **Utilisation des options de charge Ply**
Le code ci-dessous montre comment définir les options de chargement avant de charger un modèle PLY.

{{< highlight "java" >}}
// the path to the documents directory.
String MyDir = RunExamples.getDataDir();
// initialize Scene class object
Scene scene = new Scene();
// initialize an object
PlyLoadOptions loadPLYOpts = new PlyLoadOptions();
// Flip the coordinate system.
loadPLYOpts.setFlipCoordinateSystem(true);
// load 3D Ply model
scene.open(MyDir + "vase-v2.ply", loadPLYOpts);
{{< /highlight >}}
###  **Utilisation des options de charge DirectX X**
Le code ci-dessous montre comment définir les options de chargement avant de charger un fichier DirectX X.

{{< highlight "java" >}}
// the path to the documents directory.
String MyDir = RunExamples.getDataDir();
// initialize Scene class object
Scene scene = new Scene();
// initialize an object
XLoadOptions loadXOpts = new XLoadOptions(FileContentType.ASCII);
// flip the coordinate system.
loadXOpts.setFlipCoordinateSystem(true);
// load 3D X file
scene.open(MyDir + "warrior.x", loadXOpts);
{{< /highlight >}}
###  **Utiliser FBX Options de chargement**
{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java
String dataDir = RunExamples.getDataDir();
//This will output all properties defined in GlobalSettings in FBX file.
Scene scene = new Scene();
FBXLoadOptions opt = new FBXLoadOptions();
opt.setKeepBuiltinGlobalSettings(true);
scene.open(dataDir + "test.FBX", opt);
for(Property property:scene.getRootNode().getAssetInfo().getProperties())
{
    System.out.println(property);
}

{{< /highlight >}}
