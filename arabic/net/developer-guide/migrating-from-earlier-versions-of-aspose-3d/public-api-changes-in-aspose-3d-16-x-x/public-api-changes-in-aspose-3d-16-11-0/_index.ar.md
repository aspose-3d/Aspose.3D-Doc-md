---
title: العام API التغييرات في Aspose.3D 16.11.0
type: docs
weight: 20
url: /ar/net/public-api-changes-in-aspose-3d-16-11-0/
---
**Contents Sأوماري**

- [تضيف طريقة addenity في فئة Aspose.ThreeD.Node](#PublicAPIChangesinAspose.3D16.11.0-AddsAddEntityMethodintheAspose.ThreeD.NodeClass)
- [استيراد وتصدير ملفات glTF](#PublicAPIChangesinAspose.3D16.11.0-ImportandExportofglTFFiles) 
-[تضيف Aspose.ThreeD.Formats.GLTFLoadOptions Class](#PublicAPIChangesinAspose.3D16.11.0-AddsAspose.ThreeD.Formats.GLTFLoadOptionsClass)
-[يضيف Aspose.ThreeD.Formats.GLTFSaveOptions Class](#PublicAPIChangesinAspose.3D16.11.0-AddsAspose.ThreeD.Formats.GLTFSaveOptionsClass)
-[يضيف إدخال تنسيق glTF في فئة Aspose.ThreeD.FileFormat](#PublicAPIChangesinAspose.3D16.11.0-AddsglTFFormatEntryintheAspose.ThreeD.FileFormatClass)
-[إضافة خاصية تمديد في فئة Aspose.ThreeD.FileFormatType](#PublicAPIChangesinAspose.3D16.11.0-AddsanExtensionpropertyintheAspose.ThreeD.FileFormatTypeClass)
- [Rطقوس النتوءات في Rial ile ile Syالجذعية](#PublicAPIChangesinAspose.3D16.11.0-WriteDependenciesintheRealFileSystem) 
-[تضيف Aspose.ThreeD. Utility. DummyFileSystem Class](#PublicAPIChangesinAspose.3D16.11.0-AddsAspose.ThreeD.Utilities.DummyFileSystemClass)
-[تضيف Aspose.ThreeD. Ulevitors. LocalFileSystem Class](#PublicAPIChangesinAspose.3D16.11.0-AddsAspose.ThreeD.Utilities.LocalFileSystemClass)
-[تضيف Aspose.ThreeD. فائدة. فئة MemoryFileSystem](#PublicAPIChangesinAspose.3D16.11.0-AddsAspose.ThreeD.Utilities.MemoryFileSystemClass)
- [تضيف خاصية نظام الملفات في فئة Aspose.ThreeD. Formes. Iofig](#PublicAPIChangesinAspose.3D16.11.0-AddsFileSystempropertyintheAspose.ThreeD.Formats.IOConfigClass)

{{% alert color="primary" %}} 

توضح هذه الوثيقة التغييرات إلى Aspose.3D API من الإصدار 16.9.0 إلى 16.11.0 ، والتي قد تكون ذات فائدة لمطوري الوحدة/التطبيقات. لا يشمل فقط الطرق العامة الجديدة والمحدثة ، ولكن أيضًا وصفًا لأي تغييرات في السلوك وراء الكواليس في Aspose.3D.

{{% /alert %}} 
###  **تضيف طريقة addenity في فئة Aspose.ThreeD.Node**
طريقة اختصار A لإضافة كيان إلى عقدة.

**Add Entity إلى قصيدة N**

{{< highlight "java" >}}

 // initialize a Scene class object

Scene scene = new Scene();

// create a node

Node sphere = scene.RootNode.CreateChildNode("sphere");

// the old way to add an entity in a node

sphere.Entities.Add(new Sphere());

//the new way to add an entity in a node

sphere.AddEntity(new Sphere());

{{< /highlight >}}
###  **استيراد وتصدير ملفات glTF**
باستخدام الإصدار الأخير (16.11.0) أو أعلى ، يمكن للمطورين استيراد وتصدير ملفات glTF إلى/من ملفات 3D المعتمدة الأخرى.
####  **تضيف Aspose.ThreeD.Formats.GLTFLoadOptions Class**
لقد أضفنا فئة GLTFLoadOptions. يساعد في استيراد ملفات glTF إلى Aspose.3D API.

**Lip الشفاه V/T exexture ordinالمرؤوس**

{{< highlight "java" >}}

 Scene scene = new Scene();

GLTFLoadOptions loadOpt = new GLTFLoadOptions();

//The default value is true, usually we don't need to change it.

//Aspose.3D will automatically flip the V/T texture coordinate during load and save.

//to make sure it's compatible with Aspose.3D

loadOpt.FlipTexCoordV = true;

scene.Open("Duck.gltf", loadOpt);

{{< /highlight >}}
####  **يضيف Aspose.ThreeD.Formats.GLTFSaveOptions Class**
لقد أضفنا فئة GLTFSaveOptions. يحدد الإعدادات عند حفظ ملف glTF.

**تضمين التبعيات داخل ملف الإخراج glTF**

{{< highlight "java" >}}

 // the code example creates a glTF file that has a sphere, and embed all assets into the target file

// usually a glTF file comes with some dependencies, a bin file for model's vertex/indices, two .glsl files for vertex/fragment shaders

// use opt.EmbedAssets to tells the aspose.3D to export scene and embed the dependencies inside the target file.

Scene scene = new Scene();

scene.RootNode.CreateChildNode("sphere", new Sphere());

GLTFSaveOptions opt = new GLTFSaveOptions(FileContentType.ASCII);

opt.EmbedAssets = true;

scene.Save("d:\\test.gltf", opt);

{{< /highlight >}}

**Use KR_ المواد _ المشتركة Extensions إلى Define المواد M**

{{< highlight "java" >}}

 // the code example creates a glTF file that has a sphere, and use KHR_materials_common extensions to define the materials

// thus no GLSL files are generated.

Scene scene = new Scene();

scene.RootNode.CreateChildNode("sphere", new Sphere());

GLTFSaveOptions opt = new GLTFSaveOptions(FileContentType.ASCII);

opt.UseCommonMaterials = true;

scene.Save("d:\\test.gltf", opt);

{{< /highlight >}}

**Customize غير سامة من Bffer إيل**

{{< highlight "java" >}}

 // the code example creates a glTF file that has a sphere, and the buffer file that defined the model to customize the filename

Scene scene = new Scene();

scene.RootNode.CreateChildNode("sphere", new Sphere());

GLTFSaveOptions opt = new GLTFSaveOptions(FileContentType.ASCII);

opt.BufferFile = "mybuf.bin";

scene.Save("d:\\test.gltf", opt);

{{< /highlight >}}

**إنشاء ملف ثنائي glTF باستخدام ملحق khrybinarye-gltf**

{{< highlight "java" >}}

 // the code example creates a binary glTF file using KHR_binary_glTF extension

Scene scene = new Scene();

// create a child node

scene.RootNode.CreateChildNode("sphere", new Sphere());

// save 3D file

scene.Save("d:\\test.glb", FileFormat.GLTF_Binary);

{{< /highlight >}}

**إنشاء ملف ثنائي glTF باستخدام ملحق khrbinary-gltf جنبا إلى جنب مع خيارات التوفير**

{{< highlight "java" >}}

 // the code example creates a binary glTF file using KHR_binary_glTF extension but allow you to configure the save options

Scene scene = new Scene();

// create a child node

scene.RootNode.CreateChildNode("sphere", new Sphere());

// use saving options

GLTFSaveOptions opt = new GLTFSaveOptions(FileContentType.Binary);

opt.UseCommonMaterials = true;

// save 3D file

scene.Save("d:\\test.glb", opt);

{{< /highlight >}}
####  **يضيف إدخال تنسيق glTF في فئة Aspose.ThreeD.FileFormat**
لقد أضفنا إدخالات تنسيق ثنائية بقيمة GLTF و gltf-binary لأغراض التحميل والتوفير.
####  **إضافة خاصية تمديد في فئة Aspose.ThreeD.FileFormatType**
وأضاف We خاصية Extension في فئة ype ileFormatType للحصول على اسم تمديد تنسيق الملف.
###  **Rطقوس النتوءات في Rial ile ile Syالجذعية**
باستخدام الإصدار الأخير (16.11.0) أو أعلى ، يمكن للمطورين حفظ جميع تبعيات المشهد 3D في نظام الملفات الحقيقي. يمكن للمطورين تحديد مسار دليل محلي ، أو حفظ كائن نظام الذاكرة أو تجاهل التبعيات ببساطة. تتم إضافة خاصية نظام الملفات في جميع فئات خيارات الحفظ.
####  **تضيف Aspose.ThreeD. Utility. DummyFileSystem Class**
**Discard aving aving المواد iles iles**

{{< highlight "java" >}}

 // the code example uses the DummyFileSystem, so the material files are not created.

Scene scene = new Scene();

// create a child node

scene.RootNode.CreateChildNode("sphere", new Sphere()).Material = new PhongMaterial();

// set saving options

ObjSaveOptions opt = new ObjSaveOptions();

opt.FileSystem = new DummyFileSystem();

// save 3D scene

scene.Save("d:\\test.obj", opt);

{{< /highlight >}}
####  **تضيف Aspose.ThreeD. Ulevitors. LocalFileSystem Class**
**Cies ave epفي Lثماني D**

{{< highlight "java" >}}

 // the code example uses the LocalFileSystem class to save dependencies to the local directory.

Scene scene = new Scene();

// create a child node

scene.RootNode.CreateChildNode("sphere", new Sphere()).Material = new PhongMaterial();

// set saving options

ObjSaveOptions opt = new ObjSaveOptions();

opt.FileSystem = new LocalFileSystem("E:\\");

// save 3D scene

scene.Save("d:\\test.obj", opt);

{{< /highlight >}}
####  **تضيف Aspose.ThreeD. فائدة. فئة MemoryFileSystem**
**Cies افي epependenفي ememoryFileSyالجذعية bحقن**

{{< highlight "java" >}}

 // the code example uses the MemoryFileSystem to intercepts the dependencies writing.

Scene scene = new Scene();

// create a child node

scene.RootNode.CreateChildNode("sphere", new Sphere()).Material = new PhongMaterial();

// set saving options

ObjSaveOptions opt = new ObjSaveOptions();

MemoryFileSystem mfs = new MemoryFileSystem();

opt.FileSystem = mfs;

// save 3D scene

scene.Save("d:\\test.obj", opt);

//get the test.mtl file content

byte[] mtl = mfs.GetFileContent("test.mtl");

File.WriteAllBytes("material.mtl", mtl);

{{< /highlight >}}
###  **تضيف خاصية نظام الملفات في فئة Aspose.ThreeD. Formes. Iofig**
لقد أضاف We خاصية ileSyالجذعية في فئة Ionononfig لكتابة التبعيات.

**Adds خاصية غير سامة**

{{< highlight "java" >}}

 Aspose.ThreeD.Utilities.FileSystem FileSystem{ get;set;}

{{< /highlight >}}
