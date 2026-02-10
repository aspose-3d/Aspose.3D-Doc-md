---
title: Ange 3D Ladda alternativ för filName
type: docs
weight: 10
url: /sv/java/specify-3d-file-load-options/
description: Det finns flera Scene.open metod överbelastningar eller Scene klass konstruktor överbelastningar som accepterar LoadOptions instans.
---
##  **3D Ladda ner filer**
Det finns flera Scene.open metod överbelastningar eller Scene klass konstruktor överbelastningar som accepterar LoadOptions instans. Detta bör vara en instans av en klass som härrör från klassen LoadOptions. Varje belastningsformat har en motsvarande klass som innehåller belastningsalternativ för det belastningsformatet. till exempel finns det ColladaSaveOptions for the FileFormat. COLLADA spara format.
###  **Use of the Discreet 3DS Load Options**
Koden nedan visar hur laddningsalternativ ska ställas innan en diskret 3DS-fil lads in.

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
###  **Användning av Obj-lastalternativ**
Koden nedan visar hur laddningsalternativ ska ställas innan du laddar en 3D Obj-fil.

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
###  **Användning av laddandealternativ för STLName**
Koden nedan visar hur laddningsalternativ ska ställas innan du laddar en STL-fil.

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
###  **Användning av laddandealternativ för U3DName**
Koden nedan visar hur laddningsalternativ ska ställas innan du laddar en U3D-fil.

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
###  **Användning av laddandealternativ för glTFName**
Koden nedan visar hur laddningsalternativ ska ställas innan du laddar en glTF-fil.
####  **Vänd V/T texturkoordinat**
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
###  **Användning av Ply-lastalternativ**
Koden nedan visar hur laddningsalternativ ska anges innan du laddar en PLY-modell.

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
###  **Användning av DirectX X-lastalternativ**
Koden nedan visar hur man ställer in laddningsalternativ innan man laddar en DirectX-fil.

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
###  **Use FBX Load Options**
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
