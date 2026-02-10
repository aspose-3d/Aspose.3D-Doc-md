---
title: تحديد خيارات تحميل الملفات 3D بـ C#
linktitle: تحديد خيارات تحميل الملفات 3D
type: docs
weight: 30
url: /ar/net/specify-3d-file-load-options/
description: Tهنا العديد من method cene. cenطريقة القلم الزائد أو overcene الفئة منشئ الأحمال الزائدة التي تقبل كائن ptions oadO. تنسيق تحميل ach ach لديه فئة المقابلة التي تحمل خيارات الحمل لتنسيق الحمل هذا.
---
##  **Oفيرفيو**

توضح هذه المقالة كيف يمكنك تحميل أنواع مختلفة من ملفات 3D باستخدام فئات خيارات التحميل الخاصة بها في C# داخل كائن المشهد ثم يمكنك [حفظه بتنسيقات ملفات مختلفة مدعومة بقيمة 3D](https://docs.aspose.com/3d/net/specify-3d-file-save-options/). عن طريق التحميل والحفظ ، يمكنك تنفيذ عدد من التحويلات المختلفة على سبيل المثال

- تحويل FBX إلى OBJ في C#
- تحويل 3DS إلى FBX في C#
- تحويل U3D إلى OBJ في C#
- تحويل OBJ إلى 3DS في C#
- تحويل X إلى 3DS في C#

##  **خيارات تحميل الملفات 3D**
هناك العديد من الأحمال الزائدة للطرق [`Scene.Open`](https://reference.aspose.com/3d/net/aspose.threed/scene) أو الأحمال الزائدة لمُنشئ فئة المشهد التي تقبل كائن `LoadOptions`. يجب أن يكون هذا موضوعًا لفئة مشتقة من فئة `LoadOptions`. يحتوي كل تنسيق تحميل على فئة مقابلة تحتوي على خيارات تحميل لتنسيق التحميل هذا ، على سبيل المثال هناك `ColladaSaveOptions` لتنسيق الحفظ `FileFormat.Collada`.
###  **استخدام خيارات التحميل السرية 3DS**
يوضح رمز C# أدناه كيفية تعيين خيارات التحميل قبل تحميل ملف 3DS سري.

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
###  **Use من ptions bj ptions oad ptions**
يوضح رمز C# أدناه كيفية تعيين خيارات التحميل قبل تحميل ملف Obj 3D.

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
###  **استخدام خيارات التحميل STL**
يوضح رمز C# أدناه كيفية تعيين خيارات التحميل قبل تحميل ملف STL.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize an object
StlLoadOptions loadSTLOpts = new StlLoadOptions();
// Flip the coordinate system.
loadSTLOpts.FlipCoordinateSystem = true;
// Configure the look up paths to allow importer to find external dependencies.
loadSTLOpts.LookupPaths = new List<string>(new string[] { "textures" });

{{< /highlight >}}
###  **استخدام خيارات التحميل U3D**
يوضح رمز C# أدناه كيفية تعيين خيارات التحميل قبل تحميل ملف U3D.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize an object
U3dLoadOptions loadU3DOpts = new U3dLoadOptions();
// Flip the coordinate system.
loadU3DOpts.FlipCoordinateSystem = true;
// Configure the look up paths to allow importer to find external dependencies.
loadU3DOpts.LookupPaths = new List<string>(new string[] { "textures" });

{{< /highlight >}}
###  **استخدام خيارات التحميل glTF**
يوضح رمز C# أدناه كيفية تعيين خيارات التحميل قبل تحميل ملف glTF.
####  **Lip الشفاه V/T exexture ordinالمرؤوس**
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
###  **Use من ptions ly ptions oad ptions**
يوضح رمز C# أدناه كيفية تعيين خيارات التحميل قبل تحميل نموذج PLY.

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
###  **Use من ptions iptions ptions ptions oad ptions**
يوضح رمز C# أدناه كيفية تعيين خيارات التحميل قبل تحميل ملف DirectX X.

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
###  **استخدام خيارات تحميل RVM**
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
###  **باستخدام خيارات تحميل FBX**
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
