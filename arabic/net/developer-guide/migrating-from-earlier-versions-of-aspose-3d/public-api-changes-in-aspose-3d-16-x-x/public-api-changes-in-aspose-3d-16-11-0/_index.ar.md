---
title: Hangublic API hangمعلقة في Aspose.3D 16.11.0
type: docs
weight: 20
url: /ar/net/public-api-changes-in-aspose-3d-16-11-0/
---
**Contents Sأوماري**

- [Adds ddddEntity Method في Aspose.ThreeD.](#PublicAPIChangesinAspose.3D16.11.0-AddsAddEntityMethodintheAspose.ThreeD.NodeClass)
- [Import و Export من glTF iles](#PublicAPIChangesinAspose.3D16.11.0-ImportandExportofglTFFiles) 
  - [Adds Aspose.ThreeD. ororالحصير. GLTptions ptions oadOptions lass](#PublicAPIChangesinAspose.3D16.11.0-AddsAspose.ThreeD.Formats.GLTFLoadOptionsClass)
  - [Adds Aspose.ThreeD. ororالحصير. GLTptions ptions aveOptions lass](#PublicAPIChangesinAspose.3D16.11.0-AddsAspose.ThreeD.Formats.GLTFSaveOptionsClass)
  - [Adds glTF orormat nntry في Aspose.ThreeD.FileFormat lass](#PublicAPIChangesinAspose.3D16.11.0-AddsglTFFormatEntryintheAspose.ThreeD.FileFormatClass)
  - [Adds خاصية Eفي Aspose.ThreeD.FileFormatType lass](#PublicAPIChangesinAspose.3D16.11.0-AddsanExtensionpropertyintheAspose.ThreeD.FileFormatTypeClass)
- [Rطقوس النتوءات في Rial ile ile Syالجذعية](#PublicAPIChangesinAspose.3D16.11.0-WriteDependenciesintheRealFileSystem) 
  - [Adds Aspose.ThreeD.](#PublicAPIChangesinAspose.3D16.11.0-AddsAspose.ThreeD.Utilities.DummyFileSystemClass)
  - [Adds Aspose.ThreeD. tiliتيليتيز.](#PublicAPIChangesinAspose.3D16.11.0-AddsAspose.ThreeD.Utilities.LocalFileSystemClass)
  - [Adds Aspose.ThreeD.](#PublicAPIChangesinAspose.3D16.11.0-AddsAspose.ThreeD.Utilities.MemoryFileSystemClass)
- [Property dds property ileSyالجذعية الملكية في Aspose.ThreeD. orormat. IOononfig lass](#PublicAPIChangesinAspose.3D16.11.0-AddsFileSystempropertyintheAspose.ThreeD.Formats.IOConfigClass)

{{% alert color="primary" %}} 

يصف المستند الخاص به التغييرات على Aspose.3D API من الإصدار 16.9.0 إلى 16.11.0 ، والتي قد تكون ذات أهمية لمطوري الوحدات/التطبيقات. يتضمن It ليس فقط الأساليب العامة الجديدة والمحدثة ، ولكن أيضا وصفا لأي تغييرات في السلوك وراء الكواليس في Aspose.3D.

{{% /alert %}} 
### **Adds ddddEntity Method في Aspose.ThreeD.**
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
### **Import و Export من glTF iles**
Uالغناء الإصدار الأخير (16.11.0) أو أعلى ، يمكن للمطورين استيراد وتصدير الملفات glTF إلى/من الملفات الأخرى المدعومة 3D.
#### **Adds Aspose.ThreeD. ororالحصير. GLTptions ptions oadOptions lass**
لقد أضاف We فئة ptions ptions ptions ptions ptions. It يساعد في استيراد الملفات glTF إلى Aspose.3D API.

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
#### **Adds Aspose.ThreeD. ororالحصير. GLTptions ptions aveOptions lass**
لقد أضاف We فئة ptions ptions ptions ptions ptions aveO. It يحدد الإعدادات على حفظ ملف glTF.

**Embed epependennnside ututplace glTF ile ile**

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

**Cيعيد 07البولي glTF ile ile باستخدام KHR_binary_glTF xx**

{{< highlight "java" >}}

 // the code example creates a binary glTF file using KHR_binary_glTF extension

Scene scene = new Scene();

// create a child node

scene.RootNode.CreateChildNode("sphere", new Sphere());

// save 3D file

scene.Save("d:\\test.glb", FileFormat.GLTF_Binary);

{{< /highlight >}}

**Cيعيد 07البولي glTF ile ile باستخدام KHR_binary_glTF xxtension جنبا إلى جنب مع ptions aving ptions**

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
#### **Adds glTF orormat nntry في Aspose.ThreeD.FileFormat lass**
وأضاف We إدخالات تنسيق البولي GLTF و GLTF_Bلأغراض التحميل وحفظ.
#### **Adds خاصية Eفي Aspose.ThreeD.FileFormatType lass**
وأضاف We خاصية Extension في فئة ype ileFormatType للحصول على اسم تمديد تنسيق الملف.
### **Rطقوس النتوءات في Rial ile ile Syالجذعية**
Uالغناء الإصدار الأخير (16.11.0) أو أعلى ، يمكن للمطورين حفظ جميع التبعيات المشهد 3D في نظام الملفات الحقيقي. قد Dإيفليورز تحديد مسار الدليل المحلي ، حفظ في الكائن إيموريس إيليستيم أو ببساطة تجاهل التبعيات. يتم إضافة property he ilileSyالجذعية الملكية في جميع الطبقات خيار حفظ.
#### **Adds Aspose.ThreeD.**
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
#### **Adds Aspose.ThreeD. tiliتيليتيز.**
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
#### **Adds Aspose.ThreeD.**
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

byte[]mtl = mfs.GetFileContent("test.mtl");

File.WriteAllBytes("material.mtl", mtl);

{{< /highlight >}}
### **Property dds property ileSyالجذعية الملكية في Aspose.ThreeD. orormat. IOononfig lass**
لقد أضاف We خاصية ileSyالجذعية في فئة Ionononfig لكتابة التبعيات.

**Adds خاصية غير سامة**

{{< highlight "java" >}}

 Aspose.ThreeD.Utilities.FileSystem FileSystem{ get;set;}

{{< /highlight >}}
