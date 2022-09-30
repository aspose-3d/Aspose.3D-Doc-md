---
title: Hangublic API hangمعلقة في Aspose.3D 1.3.0
type: docs
weight: 40
url: /ar/net/public-api-changes-in-aspose-3d-1-3-0/
---
**Contents Sأوماري**

- [Amamespace وتغيير اسم الفئة](#PublicAPIChangesinAspose.3D1.3.0-Namespaceandclassnamechanges)
- [Create Vertex من قبل sssignature محيط Rapping apping o](#PublicAPIChangesinAspose.3D1.3.0-CreateVertexbyAssigningtheReferenceandMappingModes)
- [Universal 3D يتم إضافة ption aving ption في orileFormat](#PublicAPIChangesinAspose.3D1.3.0-Universal3DSavingOptionisaddedintheFileFormat)
- [Embed aw aw Cعلى السطح الأمامي من FBX](#PublicAPIChangesinAspose.3D1.3.0-EmbedRawContenttotheTextureofFBX)
- [يتم إضافة طريقة ececompose في فئة atriatrix4](#PublicAPIChangesinAspose.3D1.3.0-DecomposemethodisaddedintheMatrix4class)
- [يتم إضافة construcمنشئ جديد في فئة Vector4 لتلقي معلمة كائن Vector3](#PublicAPIChangesinAspose.3D1.3.0-AnewconstructorinVector4classisaddedtoreceiveaVector3objectparameter)

{{% alert color="primary" %}} 

يصف المستند الخاص به التغييرات على Aspose.3D API من الإصدار 1.2.0 إلى 1.3.0 ، والتي قد تكون ذات أهمية لمطوري الوحدات/التطبيقات. يتضمن It ليس فقط الأساليب العامة الجديدة والمحدثة ، ولكن أيضا وصفا لأي تغييرات في السلوك وراء الكواليس في Aspose.3D.

{{% /alert %}} 
### **Amamespace وتغيير اسم الفئة**
- تم تغيير nimamespace Aspose.ThreeD. nimnimation إلى Aspose.ThreeD.
- Clas Aspose.ThreeD. nimnimations. nimnimation تغيرت إلى Aspose.ThreeD. nimnimation. nimnimationNode
- تغيير Namespace Aspose.ThreeD.IO إلى Aspose.ThreeD.
- تغيير تيلز amamespace Aspose.ThreeD. Uإلى Aspose.ThreeD.
### **Create Vertex من قبل sssignature محيط Rapping apping o**
Dإيفليرز يمكن أن تخلق فيرتكس عن طريق تعيين محيط Rووضع الربط Mفي خط واحد من التعليمات البرمجية. Eرمز xample:

{{% alert color="primary" %}} 

يتم استخدام كائن الطبقة في الرمز. We يمكن[إنشاء كائن فئة Mesh كما روى هناك](/pages/createpage.action?spaceKey=3dnet&title=Create+a+3D+Cube+Mesh&linkCreation=true&fromPageId=19923253).

{{% /alert %}} 

**C#**

{{< highlight "csharp" >}}

 // call overloaded CreateElement method of the Mesh object

VertexElementNormal elementNormal = mesh.CreateElement(VertexElementType.Normal, MappingMode.ControlPoint, ReferenceMode.Direct) as VertexElementNormal;

{{< /highlight >}}

### **Universal 3D يتم إضافة ption aving ption في orileFormat**
تم إضافة خيار تنسيق he he Universal 3D في orileFormat enum. Eرمز xample:

**C#**

{{< highlight "csharp" >}}

 // save scene in the Universal3D format

scene.Save("C:\\temp\\Output.fbx", FileFormat.Universal3D);

{{< /highlight >}}

### **Embed aw aw Cعلى السطح الأمامي من FBX**
Tانه<tt>Cعلى خيمة</tt>الملكية قد أضيفت إلى<tt>Exexture</tt>الطبقة لتضمين المحتوى الخام في نسيج وثيقة FBX. Eرمز xample:

**C#**

{{< highlight "csharp" >}}

 // initialize Texture class object

Texture texture = new Texture();

// set file name

texture.FileName = "embedded-texture.png";

// set binary content

texture.Content = File.ReadAllBytes("c:\\test.png");

{{< /highlight >}}

### **يتم إضافة طريقة ececompose في فئة atriatrix4**
It هي وظيفة فائدة رياضية تستخدم لتحلل مصفوفة التحول آفين.
### **يتم إضافة construcمنشئ جديد في فئة Vector4 لتلقي معلمة كائن Vector3**
It يجعل من الأسهل لبناء ecector4 على أساس Vector3. Tانه القيمة الرابعة من Vector4 يعرض الطائرة ث value الافتراضية هي 1.
