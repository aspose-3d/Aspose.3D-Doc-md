---
title: Set up الأشياء الطبيعية أو UV على Cube و dd dd المواد إلى 3D nntities
type: docs
weight: 20
url: /ar/python-net/set-up-normals-or-uv-on-the-cube-and-add-material-to-3d-entities/
description: How لإنشاء حالات طبيعية أو بيانات الأشعة فوق البنفسجية على شبكة في Aspose.3D.
---
{{% alert color="primary" %}}

Aspose.3D ل Python via .NET يقدم لإدارة الأشياء الطبيعية و UV على الأشكال الهندسية. A شبكة مخازن الخصائص الرئيسية لكل قمة هي موقعها في الفضاء والعادية ، وهو ناقلات عمودي على السطح الأصلي. Tانه طبيعي هو الرئيسي لتظليل التهم. Tانه يجب أن تكون طبيعية ناقلات وحدة. Most شبكة الأشكال أيضا دعم شكل من أشكال coordinates coordinates التي هي تمثيل 2d منفصلة من شبكة "تكشفت" لإظهار ما هو جزء من خريطة نسيج ثنائي الأبعاد لتطبيقها على مضلع مختلفة من الشبكة.

{{% /alert %}} {{% alert color="primary" %}}

Tهو `Mesh` يتم استخدام كائن فئة في التعليمات البرمجية. We يمكن[إنشاء كائن فئة `Mesh` كما روى هناك](/3d/ar/python-net/create-3d-mesh-and-scene/)ثم أشر العقدة إلى هندسة Mesh بواسطة[Creating a 3D cencene](/3d/ar/net/create-3d-mesh-and-scene/).

{{% /alert %}}
## **Create Nأورمال Vectors**
To لديها نظرة بصرية جيدة على الإضاءة ، ونحن بحاجة إلى تحديد معلومات طبيعية لكل قمة ، للحصول على تفاصيل أفضل ، يمكننا أيضا استخدام خريطة طبيعية ومنتشرة (بالتأكيد يمكنك استخدام الظل/خريطة براقة) لأداء لكل بكسل العادي/اللون. يتم تحقيق معلومات A per-vertex مثل اللون العادي أو vertex من خلال `VertexElement`. In Aspose.3D يمكننا خريطة معلومات إضافية للتحكم في النقاط/المضلع فيرتكس/المضلع/الحافة ، عينة لتحديد الأشياء الطبيعية ل فيرتكس:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-SetupNormalsOnCube-SetupNormalsOnCube.py" >}}

Tيتم تعيين 8 ناقلات طبيعية إلى نقاط التحكم 8 مباشرة ، في المثال التالي ، سنقوم بعرض سيناريو أكثر تعقيدا بعض الشيء.
## **Ordinreate ordinordinordinالمرؤوسين**
Ere ere ، قمنا فقط بتحديد 4 إحداثيات V V ، ولكن تطبيقها على 24 vertices المضلع (6 face * 4 vertex لكل مضلع) باستخدام المؤشرات.
The Aspose.3D يوفر 5 وسائط رسم الخرائط:

- `CONTROL_POINT`-يتم تعيين كل بيانات إلى نقطة التحكم في الهندسة.
- `POLYGON_VERTEX`-يتم تعيين البيانات إلى قمة المضلع.
- `POLYGON`-يتم تعيين البيانات إلى المضلع.
- `EDGE`-يتم تعيين البيانات إلى الحافة.
- `ALL_SAME`-بيانات واحدة معددة للهندسة بأكملها.



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-SetupUVOnCube-SetupUVOnCube.py" >}}
## **المواد dd dd Mإلى 3D jecjec**
Aspose.3D لـ Python via .NET يسمح للمطورين باستخدام خوارزمية التظليل للحصول على تظليل دقيق ويسلط الضوء. Tانه Pهونغ لديها العديد من مدخلات الخريطة التي يمكننا استخدامها لإخفاء تأثير على عقدة. Pهيسيكيا ased ased dering (PBR) يأخذ بعض الخصائص الفيزيائية للأشياء في الاعتبار ، مثل هذا النهج يوفر مظهر المواد كما هو الحال في العالم الحقيقي.
### **Pهونغ Mالمواد مع إخراج Tل Cube**
Hen hen coordinates coordinates coordinates جاهزة للاستخدام ، يمكننا تطبيق نسيج على سطح الشبكة باستخدام المواد. Only فيرتكس اللون لا يمكن وصف تفاصيل السطح ، وهذا هو ما المواد المستخدمة ل. Here مثال على إرفاق مادة هونغ Pإلى عقدة مكعب:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-MaterialToCube-AddMaterialToCube.py" >}}

We حدد رسم الخرائط نسيج منتشر ، ولون براق مع معلمة شينينس.
### **Apply Phyبشكل هيسي ased R( PBR) Mإلى ox ox**
PBR يلعب دورا رئيسيا لصور محرك اللعبة ، مع تقديم فعالة وواقعية من التفاعلات بين الضوء والسطح عن طريق توهين السطوع scatالضوء المنعكس. Dإيفليرز يمكن استخدام Aspose.3D API لتطبيق المواد PBR على الأشياء 3D في مشهد. Tمثال التعليمات البرمجية يوضح كيفية إنشاء كائن ox ox ، ومن ثم تطبيق المواد Pox R.

**.NET, C#**

```py
import aspose.threed as a3d
# initialize a scene

scene = a3d.Scene()

# initialize PBR material object

mat = a3d.shading.PbrMaterial()

# an almost metal material

mat.metallic_factor = 0.9

# material surface is very rough

mat.roughness_factor = 0.9;

# create a box to which the material will be applied

boxNode = scene.root_node.create_child_node("box", a3d.entities.Box())

boxNode.material = mat

# save 3d scene into STL format

scene.save("PBR_Material_Box_Out.stl", a3d.FileFormat.STLASCII)

```
