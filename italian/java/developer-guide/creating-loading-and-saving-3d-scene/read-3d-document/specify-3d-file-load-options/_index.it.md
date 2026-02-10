---
title: Specificare 3D Opzioni di caricamento file
type: docs
weight: 10
url: /it/java/specify-3d-file-load-options/
description: Esistono diversi overload del metodo Scene.open o overload del costruttore di classi Scene che accettano l'istanza LoadOptions.
---
##  **3D Opzioni di caricamento file**
Esistono diversi overload del metodo Scene.open o overload del costruttore di classi Scene che accettano l'istanza LoadOptions. Questa dovrebbe essere un'istanza di una classe derivata dalla classe LoadOptions. Ogni formato di carico ha una classe corrispondente che contiene le opzioni di carico per quel formato di carico, ad esempio c' è ColladaSaveOptions per il formato di salvataggio FileFormat.COLLADA.
###  **Utilizzo delle opzioni di carico discre 3DS**
Il codice seguente mostra come impostare le opzioni di carico prima di caricare un file Discreet 3DS.

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
###  **Utilizzo delle opzioni di carico Obj**
Il codice seguente mostra come impostare le opzioni di carico prima di caricare un file Obj 3D.

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
###  **Utilizzo delle opzioni di carico STL**
Il codice seguente mostra come impostare le opzioni di carico prima di caricare un file STL.

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
###  **Utilizzo delle opzioni di carico U3D**
Il codice seguente mostra come impostare le opzioni di carico prima di caricare un file U3D.

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
###  **Utilizzo delle opzioni di carico glTF**
Il codice seguente mostra come impostare le opzioni di carico prima di caricare un file glTF.
####  **Capovolgi la Coordinata texture V/T**
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
###  **Utilizzo delle opzioni di carico Ply**
Il codice seguente mostra come impostare le opzioni di carico prima di caricare un modello PLY.

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
###  **Utilizzo delle opzioni di carico DirectX X**
Il codice seguente mostra come impostare le opzioni di carico prima di caricare un file DirectX X.

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
###  **Utilizza FBX opzioni di carico**
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
