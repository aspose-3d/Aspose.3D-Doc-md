---
title: Hangublic API hangمعلقة في Aspose.3D 16.9.0
type: docs
weight: 30
url: /ar/net/public-api-changes-in-aspose-3d-16-9-0/
---
**Contents Sأوماري**

- [Import 3D cencene من 07ource PDF](#PublicAPIChangesinAspose.3D16.9.0-Import3DScenefromtheSourcePDF) 
  - [Adds Aspose.ThreeD. orormat. dfdfLoadOptions lass](#PublicAPIChangesinAspose.3D16.9.0-AddsAspose.ThreeD.Formats.PdfLoadOptionsClass)
  - [Adds Aspose.ThreeD. orileFormat و Aspose.ThreeD. orormat. dfdfFormat C](#PublicAPIChangesinAspose.3D16.9.0-AddsAspose.ThreeD.FileFormatandAspose.ThreeD.Formats.PdfFormatClass)
- [Save a 3D cencene في PDF orormat](#PublicAPIChangesinAspose.3D16.9.0-Savea3DSceneinthePDFFormat) 
  - [Adds Aspose.ThreeD](#PublicAPIChangesinAspose.3D16.9.0-AddsAspose.ThreeD.Formats.PdfSaveOptionsclassandAspose.ThreeD.Formats.PdfLightingScheme/PdfRenderModeEnums)
- [Adds riريانغولي Method في Aspose.ThreeD. nntities.](#PublicAPIChangesinAspose.3D16.9.0-AddsTriangulateMethodintheAspose.ThreeD.Entities.PolygonModifierClass)
- [Adds اثنين من thouildTangentBالأمراض غير الطبيعية في Aspose.ThreeD.](#PublicAPIChangesinAspose.3D16.9.0-AddstwoBuildTangentBinormalMethodsintheAspose.ThreeD.Entities.PolygonModifierClass)

{{% alert color="primary" %}} 

يصف المستند الخاص به التغييرات على Aspose.3D API من الإصدار 2.1.0 إلى 16.9.0 ، والتي قد تكون ذات أهمية لمطوري الوحدات/التطبيقات. يتضمن It ليس فقط الأساليب العامة الجديدة والمحدثة ، ولكن أيضا وصفا لأي تغييرات في السلوك وراء الكواليس في Aspose.3D.

{{% /alert %}} 
### **Import 3D cencene من 07ource PDF**
Uالغناء الإصدار الأخير (16.9.0) أو أعلى ، يمكن للمطورين استرداد 3D مشاهد من ملف الإدخال PDF.
#### **Adds Aspose.ThreeD. orormat. dfdfLoadOptions lass**
لقد أضاف We فئة ptions dfLoadO. It يساعد في تحميل المحتوى من ملف الإدخال PDF. قد تطبق opers evelكلمة المرور ل protected protected protected المحمية s.

**Oمشهد القلم من ملف PDF محمية بكلمة مرور**

{{< highlight "java" >}}

 // set path with filename and extension 

string path = @"House_Design.pdf";

// create a new scene

Scene scene = new Scene();

// use loading options and apply password

PdfLoadOptions opt = new PdfLoadOptions() {Password = Encoding.UTF8.GetBytes("password")};

// open scene

scene.Open(path, opt);

{{< /highlight >}}
#### **Adds Aspose.ThreeD. orileFormat و Aspose.ThreeD. orormat. dfdfFormat C**
لقد أضاف We إدخال تنسيق PDF في فئة orileFormat لأغراض التحميل saving. Tانه PdfFormat الطبقة يساعد على التلاعب PPFs.

{{< highlight "java" >}}

 public static readonly Aspose.ThreeD.Formats.PdfFormat PDF;

{{< /highlight >}}

**Extract جميع المحتويات الخام 3D من ملف PDF**

{{< highlight "java" >}}

 // set PDF file path and password

string path = @"House_Design.pdf";

byte[]password = null;

// extract 3D contents

List<byte[]> contents = FileFormat.PDF.Extract(path, password);

int i = 1;

// iterate through the contents and in separate 3D files

foreach (byte[]content in contents)

{

    string fileName = "3d-" + (i++);

    File.WriteAllBytes(fileName, content);

}

{{< /highlight >}}

**Extract جميع مشاهد 3D وحفظها في ملف FBX**

{{< highlight "java" >}}

 // set PDF file path and password

string path = @"House_Design.pdf";

byte[]password = null;

List<Scene> scenes = FileFormat.PDF.ExtractScene(path, password);

int i = 1;

// iterate through the scenes and save in 3D files

foreach (Scene scene in scenes)

{

    string fileName = "3d-" + (i++) + ".fbx";

    scene.Save(fileName, FileFormat.FBX7400ASCII);

}

{{< /highlight >}}
### **Save a 3D cencene في PDF orormat**
Uالغناء الإصدار الأخير (16.9.0) أو أعلى ، يمكن للمطورين حفظ جميع الملفات المدعومة 3D في تنسيق PDF.
#### **Adds Aspose.ThreeD**
يساعد ptions he dfdfSaveOفي تطبيق الإعداد قبل الحفظ في تنسيق الإخراج PDF. Dإيفليرز يمكن تعيين وضع تقديم ونظام الإضاءة قبل توفير مشهد 3D في تنسيق PDF على النحو التالي:

**Rereate 3D PDF مع اسطوانة ، وقدمت في وضع التوضيح المظلل مع CAD الإضاءة الأمثل**

{{< highlight "java" >}}

 // create a new scene

Scene scene = new Scene();

// create a cylinder child node

scene.RootNode.CreateChildNode("cylinder", new Cylinder()).Material = new PhongMaterial() { DiffuseColor = new Vector3(Color.DarkCyan)};

// set rendering mode and lighting scheme

PdfSaveOptions opt = new PdfSaveOptions();

opt.LightingScheme = PdfLightingScheme.CAD;

opt.RenderMode = PdfRenderMode.ShadedIllustration;

// save in the PDF format

scene.Save("output.pdf", opt);

{{< /highlight >}}
### **Adds riريانغولي Method في Aspose.ThreeD. nntities.**
وقد أضاف We الزائد آخر من طريقة ريانغويتي في فئة أوديفييه أوليغونغونغ التي تأخذ كائن فئة cenسين كمعلمة.

**Convert جميع المضلعات إلى مثلثات في ملف FBX**

{{< highlight "java" >}}

 // load an existing 3D file

Scene scene = new Scene("original.fbx");

// triangulate a scene

PolygonModifier.Triangulate(scene);

// save 3D scene

scene.Save("triangulated.fbx", FileFormat.FBX7400ASCII);

{{< /highlight >}}
### **Adds اثنين من thouildTangentBالأمراض غير الطبيعية في Aspose.ThreeD.**
لقد أضاف We اثنين من الطرق غير الطبيعية في الطرق غير الطبيعية في فئة أوديفير أوليغونديفير. طريقة ne ne تأخذ كائن فئة cencene كمعلمة وآخر يأخذ كائن فئة Mesh كمعلمة.

**Build بيانات متشابكة وبينورمال لجميع تنسجم في ملف FBX**

{{< highlight "java" >}}

 // load an existing 3D file

Scene scene = new Scene("original.fbx");

// triangulate a scene

PolygonModifier.BuildTangentBinormal(scene);

// save 3D scene

scene.Save("output.fbx", FileFormat.FBX7400ASCII);

{{< /highlight >}}
