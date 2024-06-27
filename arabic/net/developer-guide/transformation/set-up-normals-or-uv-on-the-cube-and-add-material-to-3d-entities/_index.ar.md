---
title: إعداد المواد العادية أو الأشعة فوق البنفسجية على المكعب وإضافة المواد إلى الكيانات 3D
type: docs
weight: 20
url: /ar/net/set-up-normals-or-uv-on-the-cube-and-add-material-to-3d-entities/
description: How to create normals or uv data on a mesh in Aspose.3D.
---
{{% alert color="primary" %}}

Aspose.3D for .NET عروض لإدارة الأمور العادية وفوق البنفسجية على الأشكال الهندسية. تخزن الشبكة الخصائص الرئيسية لكل قمة هي موضعها في الفضاء وطبيعته ، متجه عمودي على السطح الأصلي. الطبيعي هو كبير لكميات التظليل. يجب أن تكون الوحدات العادية موجهات. تدعم معظم تنسيقات الشبكات أيضًا بعض أشكال إحداثيات الموجات فوق الصوتية التي تمثل تمثيلًا منفصلاً ثنائي الأبعاد للشبكة "غير مطوي" لإظهار أي جزء من خريطة نسيج ثنائي الأبعاد لتطبيقه على مضلعات مختلفة من الشبكة.

{{% /alert %}} {{% alert color="primary" %}}

كائن الفئة `Mesh` قيد الاستخدام في الرمز. يمكننا [إنشاء كائن فئة Mesh كما روى هناك](/3d/ar/net/create-3d-mesh-and-scene/) ثم الإشارة إلى عقدة إلى هندسة الشبكة بمقدار [إنشاء مشهد 3D](/3d/ar/net/create-3d-mesh-and-scene/).

{{% /alert %}}
##  **Create Nأورمال Vectors**
للحصول على نظرة بصرية جيدة على الإضاءة ، نحتاج إلى تحديد المعلومات العادية لكل قمة ، للحصول على تفاصيل أفضل ، يمكننا أيضًا استخدام خريطة عادية ومنتشرة (تأكد من أنه يمكنك استخدام خريطة ظل/منظر) لأداء كل بكسل عادي/لون. يتم تحقيق معلومات لكل قمة الرأس مثل اللون العادي أو الرأس بواسطة VertexElement. في Aspose.3D يمكننا رسم معلومات إضافية للتحكم في النقاط/الرأس المضلع/المضلع/الحافة ، عينة لتحديد الحالات العادية للقمة:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Geometry-and-Hierarchy-SetupNormalsOnCube-SetupNormalsOnCube.cs" >}}

Tيتم تعيين 8 ناقلات طبيعية إلى نقاط التحكم 8 مباشرة ، في المثال التالي ، سنقوم بعرض سيناريو أكثر تعقيدا بعض الشيء.
##  **Ordinreate ordinordinordinالمرؤوسين**
Ere ere ، قمنا فقط بتحديد 4 إحداثيات V V ، ولكن تطبيقها على 24 vertices المضلع (6 face * 4 vertex لكل مضلع) باستخدام المؤشرات.
يوفر Aspose.3D 5 أوضاع تعيين:

- `ControlPoint` -يتم تعيين كل بيانات إلى نقطة التحكم في الهندسة.
- `PolygonVertex` -تم تعيين البيانات إلى قمة المضلع.
- `Polygon` -تم تعيين البيانات إلى المضلع.
- `Edge` -تم تعيين البيانات إلى الحافة.
- `AllSame` -تم تعيين بيانات واحدة إلى الهندسة بأكملها.



{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Geometry-and-Hierarchy-SetupUVOnCube-SetupUVOnCube.cs" >}}
##  **إضافة مواد إلى منتجات 3D**
Aspose.3D for .NET يسمح للمطورين باستخدام خوارزمية التظليل لتظليل وإبراز دقيق. يحتوي الفونج على العديد من مدخلات الخرائط التي يمكننا استخدامها لإخفاء التأثير على العقدة. يأخذ التقديم القائم على أساس مادي (PBR) بعض الخصائص الفيزيائية للأشياء في الاعتبار ، ويوفر هذا النهج مظهر المواد كما هو الحال في العالم الحقيقي.
###  **Pهونغ Mالمواد مع إخراج Tل Cube**
Hen hen coordinates coordinates coordinates جاهزة للاستخدام ، يمكننا تطبيق نسيج على سطح الشبكة باستخدام المواد. Only فيرتكس اللون لا يمكن وصف تفاصيل السطح ، وهذا هو ما المواد المستخدمة ل. Here مثال على إرفاق مادة هونغ Pإلى عقدة مكعب:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Geometry-and-Hierarchy-MaterialToCube-AddMaterialToCube.cs" >}}

We حدد رسم الخرائط نسيج منتشر ، ولون براق مع معلمة شينينس.
###  **Apply Phyبشكل هيسي ased R( PBR) Mإلى ox ox**
PBR plays a key role for the game engine visuals, with its efficient and realistic rendering of interactions between light and surface via attenuation of the brightness and scattering of reflected light. Developers can use Aspose.3D API to apply PBR material to 3D objects in a scene. This code example demonstrates to how to create a Box object, and then apply the PBR material.

**.NET ، C#**

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
