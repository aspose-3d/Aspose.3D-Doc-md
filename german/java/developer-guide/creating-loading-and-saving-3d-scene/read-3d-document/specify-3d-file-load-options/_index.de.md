---
title: 3D Datei lade optionen angeben
type: docs
weight: 10
url: /de/java/specify-3d-file-load-options/
description: Es gibt mehrere Überladungen von Scene.open-Methoden oder Überladungen von Scene-Klassen konstruktoren, die die LoadOptions-Instanz akzeptieren.
---
##  **3D Datei lade optionen**
Es gibt mehrere Überladungen von Scene.open-Methoden oder Überladungen von Scene-Klassen konstruktoren, die die LoadOptions-Instanz akzeptieren. Dies sollte eine Instanz einer Klasse sein, die von der LoadOptions-Klasse abgeleitet wurde. Jedes Last format verfügt über eine entsprechende Klasse, die Last optionen für dieses Last format enthält. Beispiels weise gibt es ColladaS ave Options für das Speichern format File Format.COLLADA.
###  **Verwendung der diskreten 3DS-Lade optionen**
Der folgende Code zeigt, wie Sie Lade optionen festlegen, bevor Sie eine Discreet 3DS-Datei laden.

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
###  **Verwendung der Obj-Lade optionen**
Der folgende Code zeigt, wie Sie Lade optionen festlegen, bevor Sie eine 3D Obj-Datei laden.

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
###  **Verwendung der STL-Lade optionen**
Der folgende Code zeigt, wie Sie Lade optionen festlegen, bevor Sie eine STL-Datei laden.

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
###  **Verwendung der U3D-Lade optionen**
Der folgende Code zeigt, wie Sie Lade optionen festlegen, bevor Sie eine U3D-Datei laden.

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
###  **Verwendung der glTF-Lade optionen**
Der folgende Code zeigt, wie Sie Lade optionen festlegen, bevor Sie eine glTF-Datei laden.
####  **Drehen Sie die V/T-Textur koordination um**
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
###  **Verwendung der Ply-Load-Optionen**
Der folgende Code zeigt, wie Sie Lade optionen festlegen, bevor Sie ein PLY-Modell laden.

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
###  **Verwendung der DirectX X-Lade optionen**
Der folgende Code zeigt, wie Sie Lade optionen festlegen, bevor Sie eine DirectX X-Datei laden.

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
###  **Verwenden Sie FBX Lade optionen**
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
