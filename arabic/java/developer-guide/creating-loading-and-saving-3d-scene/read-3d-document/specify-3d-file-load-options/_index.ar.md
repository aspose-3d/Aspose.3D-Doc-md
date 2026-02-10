---
title: تحديد خيارات تحميل الملفات 3D
type: docs
weight: 10
url: /ar/java/specify-3d-file-load-options/
description: Tهنا العديد من overcene. open طريقة الأحمال الزائدة أو overcene الفئة منشئ الأحمال الزائدة التي تقبل ptions oadOسبيل المثال.
---
##  **خيارات تحميل الملفات 3D**
Tهنا العديد من overcene. open طريقة الأحمال الزائدة أو overcene الفئة منشئ الأحمال الزائدة التي تقبل ptions oadOسبيل المثال. Tيجب أن يكون مثال على فئة مشتقة من فئة ptions oadO. تنسيق تحميل ach ach لديه فئة المقابلة التي تحمل خيارات الحمل لذلك تنسيق الحمل ، على سبيل المثال هناك ptions olladaSaveOوصفات ل ilileFormat. COLAsave حفظ تنسيق.
###  **استخدام خيارات التحميل السرية 3DS**
يوضح الرمز أدناه كيفية تعيين خيارات التحميل قبل تحميل ملف منفصل 3DS.

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
###  **Use من ptions bj ptions oad ptions**
يوضح الرمز أدناه كيفية تعيين خيارات التحميل قبل تحميل ملف Obj 3D.

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
###  **استخدام خيارات التحميل STL**
يوضح الرمز أدناه كيفية تعيين خيارات التحميل قبل تحميل ملف STL.

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
###  **استخدام خيارات التحميل U3D**
يوضح الرمز أدناه كيفية تعيين خيارات التحميل قبل تحميل ملف U3D.

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
###  **استخدام خيارات التحميل glTF**
يوضح الرمز أدناه كيفية تعيين خيارات التحميل قبل تحميل ملف glTF.
####  **Lip الشفاه V/T exexture ordinالمرؤوس**
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
###  **Use من ptions ly ptions oad ptions**
يوضح الرمز أدناه كيفية تعيين خيارات التحميل قبل تحميل نموذج PLY.

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
###  **Use من ptions iptions ptions ptions oad ptions**
Tانه رمز أدناه يظهر كيفية تعيين خيارات التحميل قبل تحميل ملف Diمستطيل X.

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
###  **استخدام خيارات تحميل FBX**
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
