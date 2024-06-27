---
title: العام API التغييرات في Aspose.3D 16.9.0
type: docs
weight: 30
url: /ar/net/public-api-changes-in-aspose-3d-16-9-0/
---
**Contents Sأوماري**

- [استورد مشهد 3D من المصدر PDF](#PublicAPIChangesinAspose.3D16.9.0-Import3DScenefromtheSourcePDF) 
-[يضيف Aspose.ThreeD. Formules. PdfLoadOptions Class](#PublicAPIChangesinAspose.3D16.9.0-AddsAspose.ThreeD.Formats.PdfLoadOptionsClass)
-[تضيف Aspose.ThreeD.FileFormat و Aspose.ThreeD.Formats.PdfFormat Class](#PublicAPIChangesinAspose.3D16.9.0-AddsAspose.ThreeD.FileFormatandAspose.ThreeD.Formats.PdfFormatClass)
- [توفير مشهد 3D بتنسيق PDF](#PublicAPIChangesinAspose.3D16.9.0-Savea3DSceneinthePDFFormat) 
-[يضيف Aspose.ThreeD.Formats.PdfSaveOptions class و Aspose.ThreeD.Formats.PdfLightingScheme/PdfRenderMode](#PublicAPIChangesinAspose.3D16.9.0-AddsAspose.ThreeD.Formats.PdfSaveOptionsclassandAspose.ThreeD.Formats.PdfLightingScheme/PdfRenderModeEnums)
- [تضيف طريقة التثليث في فئة Aspose.ThreeD. Enties. PolygonModifier](#PublicAPIChangesinAspose.3D16.9.0-AddsTriangulateMethodintheAspose.ThreeD.Entities.PolygonModifierClass)
- [يضيف طريقتين buildtanentbinormal في فئة Aspose.ThreeD.Entities.PolygonModifier](#PublicAPIChangesinAspose.3D16.9.0-AddstwoBuildTangentBinormalMethodsintheAspose.ThreeD.Entities.PolygonModifierClass)

{{% alert color="primary" %}} 

يوضح هذا المستند التغييرات إلى Aspose.3D API من الإصدار 2.1.0 إلى 16.9.0 ، والتي قد تكون ذات فائدة لمطوري الوحدة/التطبيق. لا يشمل فقط الطرق العامة الجديدة والمحدثة ، ولكن أيضًا وصفًا لأي تغييرات في السلوك وراء الكواليس في Aspose.3D.

{{% /alert %}} 
###  **استورد مشهد 3D من المصدر PDF**
باستخدام الإصدار الأخير (16.9.0) أو أعلى ، يمكن للمطورين استرداد مشاهد 3D من ملف إدخال PDF.
####  **يضيف Aspose.ThreeD. Formules. PdfLoadOptions Class**
لقد أضفنا فئة PdfLoadOptions. يساعد في تحميل المحتوى من ملف الإدخال PDF. يمكن للمطورين تطبيق كلمة مرور لـ PDFs المحمية.

**مشهد مفتوح من ملف PDF المحمي بكلمة مرور**

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
####  **تضيف Aspose.ThreeD.FileFormat و Aspose.ThreeD.Formats.PdfFormat Class**
لقد أضفنا إدخال بتنسيق PDF في فئة تنسيق الملفات لأغراض التحميل والتوفير. تساعد فئة PdfFormat على التلاعب بملفات PDFs.

{{< highlight "java" >}}

 public static readonly Aspose.ThreeD.Formats.PdfFormat PDF;

{{< /highlight >}}

**استخراج كل محتويات 3D الخام من ملف PDF**

{{< highlight "java" >}}

 // set PDF file path and password

string path = @"House_Design.pdf";

byte[] password = null;

// extract 3D contents

List<byte[]> contents = FileFormat.PDF.Extract(path, password);

int i = 1;

// iterate through the contents and in separate 3D files

foreach (byte[] content in contents)

{

    string fileName = "3d-" + (i++);

    File.WriteAllBytes(fileName, content);

}

{{< /highlight >}}

**استخرج جميع مشاهد 3D وحفظها في ملف FBX**

{{< highlight "java" >}}

 // set PDF file path and password

string path = @"House_Design.pdf";

byte[] password = null;

List<Scene> scenes = FileFormat.PDF.ExtractScene(path, password);

int i = 1;

// iterate through the scenes and save in 3D files

foreach (Scene scene in scenes)

{

    string fileName = "3d-" + (i++) + ".fbx";

    scene.Save(fileName, FileFormat.FBX7400ASCII);

}

{{< /highlight >}}
###  **توفير مشهد 3D بتنسيق PDF**
باستخدام الإصدار الأخير (16.9.0) أو أعلى ، يمكن للمطورين حفظ جميع ملفات 3D المدعومة بتنسيق PDF.
####  **يضيف Aspose.ThreeD.Formats.PdfSaveOptions class و Aspose.ThreeD.Formats.PdfLightingScheme/PdfRenderMode**
يساعد PdfSaveOptions في تطبيق الإعداد قبل الحفظ في تنسيق الإخراج PDF. يمكن للمطورين تعيين وضع تقديم ونظام إضاءة قبل حفظ مشهد 3D في تنسيق PDF على النحو التالي:

**Create a 3D PDF with a cylinder, and rendered in shaded illustration mode with CAD optimized lighting**

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
###  **تضيف طريقة التثليث في فئة Aspose.ThreeD. Enties. PolygonModifier**
وقد أضاف We الزائد آخر من طريقة ريانغويتي في فئة أوديفييه أوليغونغونغ التي تأخذ كائن فئة cenسين كمعلمة.

**تحويل جميع المضلعات إلى مثلثات في ملف FBX**

{{< highlight "java" >}}

 // load an existing 3D file

Scene scene = new Scene("original.fbx");

// triangulate a scene

PolygonModifier.Triangulate(scene);

// save 3D scene

scene.Save("triangulated.fbx", FileFormat.FBX7400ASCII);

{{< /highlight >}}
###  **يضيف طريقتين buildtanentbinormal في فئة Aspose.ThreeD.Entities.PolygonModifier**
لقد أضاف We اثنين من الطرق غير الطبيعية في الطرق غير الطبيعية في فئة أوديفير أوليغونديفير. طريقة ne ne تأخذ كائن فئة cencene كمعلمة وآخر يأخذ كائن فئة Mesh كمعلمة.

**إنشاء بيانات ظلالية وثنائية الشكل لجميع الشبكات في ملف FBX**

{{< highlight "java" >}}

 // load an existing 3D file

Scene scene = new Scene("original.fbx");

// triangulate a scene

PolygonModifier.BuildTangentBinormal(scene);

// save 3D scene

scene.Save("output.fbx", FileFormat.FBX7400ASCII);

{{< /highlight >}}
