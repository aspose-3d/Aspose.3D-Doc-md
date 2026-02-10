---
title: 指定 3D 文件加载选项
type: docs
weight: 10
url: /zh/java/specify-3d-file-load-options/
description: 有几个接受loadopons实例的Scene.open方法重载或Scene类构造函数重载。
---
##  **3D 文件加载选项**
有几个接受loadopons实例的Scene.open方法重载或Scene类构造函数重载。这应该是从LoadOptions类派生的类的实例。每种加载格式都有一个相应的类，该类保存该加载格式的加载选项，例如，FileFormat.COLLADA保存格式有colladasveoptions。
###  **使用Discreet 3DS 加载选项**
下面的代码显示了如何在加载一个谨慎的 3DS 文件之前设置加载选项。

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
###  **使用Obj加载选项**
下面的代码显示了如何在加载 3D Obj文件之前设置加载选项。

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
###  **STL 加载选项的使用**
下面的代码显示了如何在加载 STL 文件之前设置加载选项。

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
###  **U3D 加载选项的使用**
下面的代码显示了如何在加载 U3D 文件之前设置加载选项。

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
###  **glTF 加载选项的使用**
下面的代码显示了如何在加载 glTF 文件之前设置加载选项。
####  **翻转V/T纹理坐标**
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
###  **使用层载荷选项**
下面的代码显示了如何在加载 PLY 模型之前设置加载选项。

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
###  **使用DirectX X加载选项**
下面的代码显示了如何在加载DirectX文件之前设置加载选项。

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
###  **使用 FBX 加载选项**
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
