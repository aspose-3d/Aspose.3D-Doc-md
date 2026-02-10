---
title: Укажите параметры загрузки файла 3D в C#
linktitle: Укажите параметры загрузки файла 3D
type: docs
weight: 30
url: /ru/net/specify-3d-file-load-options/
description: Существует несколько перегрузок метода Scene.Open или перегрузок конструктора класса Scene, которые принимают объект LoadOptions. Каждый формат нагрузки имеет соответствующий класс, который содержит параметры загрузки для этого формата нагрузки.
---
##  **Обзор**

В этой статье объясняется, как вы можете загружать различные типы файлов 3D, используя соответствующие классы опций загрузки в C# внутри объекта Scene, а затем вы можете загружать [Сохранить его в различных поддерживаемых форматах файлов 3D](https://docs.aspose.com/3d/net/specify-3d-file-save-options/). Загрузив и сохранив, вы можете выполнить ряд различных преобразований, например

- Конвертировать FBX в OBJ в C#
- Конвертировать 3DS в FBX в C#
- Конвертировать U3D в OBJ в C#
- Конвертировать OBJ в 3DS в C#
- Конвертировать X в 3DS в C#

##  **3D Параметры загрузки файла**
Существует несколько перегрузок метода [`Scene.Open`](https://reference.aspose.com/3d/net/aspose.threed/scene) или перегрузок конструктора класса Scene, которые принимают объект `LoadOptions`. Это должен быть объект класса, производного от класса `LoadOptions`. Каждый формат загрузки имеет соответствующий класс, который содержит параметры загрузки для этого формата загрузки, например, есть `ColladaSaveOptions` для формата сохранения `FileFormat.Collada`.
###  **Использование дискретных параметров загрузки 3DS**
Код C# ниже показывает, как установить параметры загрузки перед загрузкой файла Discreet 3DS.

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
###  **Использование опций нагрузки Obj**
Код C# ниже показывает, как установить параметры загрузки перед загрузкой файла 3D Obj.

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
###  **Использование параметров загрузки STL**
Код C# ниже показывает, как установить параметры загрузки перед загрузкой файла STL.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize an object
StlLoadOptions loadSTLOpts = new StlLoadOptions();
// Flip the coordinate system.
loadSTLOpts.FlipCoordinateSystem = true;
// Configure the look up paths to allow importer to find external dependencies.
loadSTLOpts.LookupPaths = new List<string>(new string[] { "textures" });

{{< /highlight >}}
###  **Использование параметров загрузки U3D**
Код C# ниже показывает, как установить параметры загрузки перед загрузкой файла U3D.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize an object
U3dLoadOptions loadU3DOpts = new U3dLoadOptions();
// Flip the coordinate system.
loadU3DOpts.FlipCoordinateSystem = true;
// Configure the look up paths to allow importer to find external dependencies.
loadU3DOpts.LookupPaths = new List<string>(new string[] { "textures" });

{{< /highlight >}}
###  **Использование параметров загрузки glTF**
Код C# ниже показывает, как установить параметры загрузки перед загрузкой файла glTF.
####  **Переверните координату текстуры V/T**
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
###  **Использование опций нагрузки Ply**
Код C# ниже показывает, как установить параметры загрузки перед загрузкой модели PLY.

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
###  **Использование опций нагрузки DirectX X**
Код C# ниже показывает, как установить параметры загрузки перед загрузкой файла DirectX X.

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
###  **Используйте параметры загрузки RVM**
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
###  **Использование параметров загрузки FBX**
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
