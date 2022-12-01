---
title: Set up الأشياء الطبيعية أو UV على Cube و dd dd المواد إلى 3D nntities
type: docs
weight: 20
url: /ar/net/set-up-normals-or-uv-on-the-cube-and-add-material-to-3d-entities/
description: How لإنشاء حالات طبيعية أو بيانات الأشعة فوق البنفسجية على شبكة في Aspose.3D.
---
{{% alert color="primary" %}}

Aspose.3D for .NET يقدم لإدارة الأشياء الطبيعية و UV على الأشكال الهندسية. A شبكة مخازن الخصائص الرئيسية لكل قمة هي موقعها في الفضاء والعادية ، وهو ناقلات عمودي على السطح الأصلي. Tانه طبيعي هو الرئيسي لتظليل التهم. Tانه يجب أن تكون طبيعية ناقلات وحدة. Most شبكة الأشكال أيضا دعم شكل من أشكال coordinates coordinates التي هي تمثيل 2d منفصلة من شبكة "تكشفت" لإظهار ما هو جزء من خريطة نسيج ثنائي الأبعاد لتطبيقها على مضلع مختلفة من الشبكة.

{{% /alert %}} {{% alert color="primary" %}}

Tهو `Mesh` يتم استخدام كائن فئة في التعليمات البرمجية. We يمكن[إنشاء كائن فئة Mesh كما روى هناك](/3d/ar/net/create-3d-mesh-and-scene/)ثم أشر العقدة إلى هندسة Mesh بواسطة[Creating a 3D cencene](/3d/ar/net/create-3d-mesh-and-scene/).

{{% /alert %}}
## **Create Nأورمال Vectors**
To لديها نظرة بصرية جيدة على الإضاءة ، ونحن بحاجة إلى تحديد معلومات طبيعية لكل قمة ، للحصول على تفاصيل أفضل ، يمكننا أيضا استخدام خريطة طبيعية ومنتشرة (بالتأكيد يمكنك استخدام الظل/خريطة براقة) لأداء لكل بكسل العادي/اللون. يتم تحقيق المعلومات A لكل درجة مثل اللون العادي أو قمة الرأس عن طريق lement ertexElement. In Aspose.3D يمكننا خريطة معلومات إضافية للتحكم في نقاط/المضلع فيرتكس/المضلع/الحافة ، عينة لتحديد الأشياء الطبيعية ل فيرتكس:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Geometry-and-Hierarchy-SetupNormalsOnCube-SetupNormalsOnCube.cs" >}}

Tيتم تعيين 8 ناقلات طبيعية إلى نقاط التحكم 8 مباشرة ، في المثال التالي ، سنقوم بعرض سيناريو أكثر تعقيدا بعض الشيء.
## **Ordinreate ordinordinordinالمرؤوسين**
Ere ere ، قمنا فقط بتحديد 4 إحداثيات V V ، ولكن تطبيقها على 24 vertices المضلع (6 face * 4 vertex لكل مضلع) باستخدام المؤشرات.
The Aspose.3D يوفر 5 وسائط رسم الخرائط:

- `ControlPoint`-يتم تعيين كل بيانات إلى نقطة التحكم في الهندسة.
- `PolygonVertex`-يتم تعيين البيانات إلى قمة المضلع.
- `Polygon`-يتم تعيين البيانات إلى المضلع.
- `Edge`-يتم تعيين البيانات إلى الحافة.
- `AllSame`-بيانات واحدة معددة للهندسة بأكملها.



{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Geometry-and-Hierarchy-SetupUVOnCube-SetupUVOnCube.cs" >}}
## **المواد dd dd Mإلى 3D jecjec**
Aspose.3D for .NET يسمح للمطورين باستخدام خوارزمية التظليل لتظليل دقيق ويبرز. Tانه Pهونغ لديها العديد من مدخلات الخريطة التي يمكننا استخدامها لإخفاء تأثير على عقدة. Pهيسيكيا ased ased dering (PBR) يأخذ بعض الخصائص الفيزيائية للأشياء في الاعتبار ، مثل هذا النهج يوفر مظهر المواد كما هو الحال في العالم الحقيقي.
### **Pهونغ Mالمواد مع إخراج Tل Cube**
Hen hen coordinates coordinates coordinates جاهزة للاستخدام ، يمكننا تطبيق نسيج على سطح الشبكة باستخدام المواد. Only فيرتكس اللون لا يمكن وصف تفاصيل السطح ، وهذا هو ما المواد المستخدمة ل. Here مثال على إرفاق مادة هونغ Pإلى عقدة مكعب:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Geometry-and-Hierarchy-MaterialToCube-AddMaterialToCube.cs" >}}

We حدد رسم الخرائط نسيج منتشر ، ولون براق مع معلمة شينينس.
### **Apply Phyبشكل هيسي ased R( PBR) Mإلى ox ox**
PBR يلعب دورا رئيسيا لصور محرك اللعبة ، مع تقديم فعالة وواقعية من التفاعلات بين الضوء والسطح عن طريق توهين السطوع scatالضوء المنعكس. Dإيفليرز يمكن استخدام Aspose.3D API لتطبيق المواد PBR على الأشياء 3D في مشهد. Tمثال التعليمات البرمجية يوضح كيفية إنشاء كائن ox ox ، ومن ثم تطبيق المواد Pox R.

**.NET, C#**

{{< highlight "java" >}}

 // initialize a scene

Scene scene = new Scene();

// initialize PBR material object

PbrMaterial mat = new PbrMaterial();

// an almost metal material

mat.MetallicFactor = 0.9;

// material surface is very rough

mat.RoughnessFactor = 0.9;

// create a box to which the material will be applied

var boxNode = scene.RootNode.CreateChildNode("box", new Box());

boxNode.Material = mat;

// save 3d scene into STL format

scene.Save(@"C:\3D\PBR_Material_Box_Out.stl", FileFormat.STLASCII);

{{< /highlight >}}
