---
title: العام API يتغير في Aspose.3D 1.3.0
type: docs
weight: 40
url: /ar/net/public-api-changes-in-aspose-3d-1-3-0/
---
**Contents Sأوماري**

- [Amamespace وتغيير اسم الفئة](#PublicAPIChangesinAspose.3D1.3.0-Namespaceandclassnamechanges)
- [Create Vertex من قبل sssignature محيط Rapping apping o](#PublicAPIChangesinAspose.3D1.3.0-CreateVertexbyAssigningtheReferenceandMappingModes)
- [تمت إضافة خيار التوفير Universal 3D في تنسيق الملف](#PublicAPIChangesinAspose.3D1.3.0-Universal3DSavingOptionisaddedintheFileFormat)
- [تضمين محتوى خام في نسيج FBX](#PublicAPIChangesinAspose.3D1.3.0-EmbedRawContenttotheTextureofFBX)
- [يتم إضافة طريقة ececompose في فئة atriatrix4](#PublicAPIChangesinAspose.3D1.3.0-DecomposemethodisaddedintheMatrix4class)
- [يتم إضافة construcمنشئ جديد في فئة Vector4 لتلقي معلمة كائن Vector3](#PublicAPIChangesinAspose.3D1.3.0-AnewconstructorinVector4classisaddedtoreceiveaVector3objectparameter)

{{% alert color="primary" %}} 

يوضح هذا المستند التغييرات إلى Aspose.3D API من الإصدار 1.2.0 إلى 1.3.0 ، والتي قد تهم مطوري الوحدات/التطبيقات. لا يشمل فقط الطرق العامة الجديدة والمحدثة ، ولكن أيضًا وصفًا لأي تغييرات في السلوك وراء الكواليس في Aspose.3D.

{{% /alert %}} 
###  **Amamespace وتغيير اسم الفئة**
- مساحة الاسم Aspose. تم تغيير الرسوم المتحركة إلى Aspose.ThreeD.Animation
- فئة Aspose.ThreeD. رسوم متحركة. تغيرت الرسوم المتحركة إلى Aspose.ThreeD.Animation.AnimationNode
- Namespace Aspose. تم تغيير ThreeD.IO إلى Aspose. تنسيقات ThreeD.
- مساحة الاسم Aspose. تم تغيير ThreeD.Utils إلى Aspose.ThreeD.Utils
###  **Create Vertex من قبل sssignature محيط Rapping apping o**
Dإيفليرز يمكن أن تخلق فيرتكس عن طريق تعيين محيط Rووضع الربط Mفي خط واحد من التعليمات البرمجية. Eرمز xample:

{{% alert color="primary" %}} 

يتم استخدام كائن فئة الشبكة في الرمز. يمكننا [إنشاء كائن فئة Mesh كما روى هناك](/pages/createpage.action?spaceKey=3dnet&title=Create+a+3D+Cube+Mesh&linkCreation=true&fromPageId=19923253).

{{% /alert %}} 

**C#**

{{< highlight "csharp" >}}

 // call overloaded CreateElement method of the Mesh object

VertexElementNormal elementNormal = mesh.CreateElement(VertexElementType.Normal, MappingMode.ControlPoint, ReferenceMode.Direct) as VertexElementNormal;

{{< /highlight >}}

###  **تمت إضافة خيار التوفير Universal 3D في تنسيق الملف**
تمت إضافة خيار تنسيق Universal 3D في قائمة الملفات. رمز المثال:

**C#**

{{< highlight "csharp" >}}

 // save scene in the Universal3D format

scene.Save("C:\\temp\\Output.fbx", FileFormat.Universal3D);

{{< /highlight >}}

###  **تضمين محتوى خام في نسيج FBX**
Tانه<tt>Cعلى خيمة</tt>الملكية قد أضيفت إلى<tt>Exexture</tt>فئة لتضمين المحتوى الخام في نسيج مستند FBX. رمز المثال:

**C#**

{{< highlight "csharp" >}}

 // initialize Texture class object

Texture texture = new Texture();

// set file name

texture.FileName = "embedded-texture.png";

// set binary content

texture.Content = File.ReadAllBytes("c:\\test.png");

{{< /highlight >}}

###  **يتم إضافة طريقة ececompose في فئة atriatrix4**
It هي وظيفة فائدة رياضية تستخدم لتحلل مصفوفة التحول آفين.
###  **يتم إضافة construcمنشئ جديد في فئة Vector4 لتلقي معلمة كائن Vector3**
It يجعل من الأسهل لبناء ecector4 على أساس Vector3. Tانه القيمة الرابعة من Vector4 يعرض الطائرة ث value الافتراضية هي 1.
