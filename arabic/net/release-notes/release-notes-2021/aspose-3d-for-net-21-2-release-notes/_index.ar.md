---
title: Aspose.3D for .NET 21.2 tes elease ootes
type: docs
weight: 11
url: /ar/net/aspose-3d-for-net-21-2-release-notes/
---
{{% alert color="primary" %}}

Tصفحته تحتوي على معلومات ملاحظات الافراج عن Aspose.3D for .NET 21.2.

{{% /alert %}}
## **Ements proو Cمعلقة**

|**Key**|**Sأوماري**|**Category**|
|:- |:- |:- |
|THREEDNET-825 |Add USDZ دعم الاستيراد.|ميزة ew ew|
|THREEDNET-824 |Add دعم الملمس في USDZ|Ask اسأل|
|THREEDNET-811 |Implement نسخة التقييم ذات الصلة xcxception في API|حركة بلا حدود|
|THREEDNET-813 |مطلوب تفاصيل Technical على المواد Mو exexture API القيود-API لا يوفر وسيلة لاكتشاف القوام على المواد|حركة بلا حدود|
|THREEDNET-817 |دعم dd dd للبايت الملمس [] في حالة glb ، gltf ، obj|حركة بلا حدود|
|THREEDAPP-80 |Improof سرعة تحميل الصفحة من بائع الويب|حركة بلا حدود|
|THREEDNET-814 |مؤشرات riangle غير صحيحة|إصلاح g ug|
|THREEDNET-809 |FBX Save Exception: نوع السمة غير المدعومة|إصلاح g ug|
|THREEDNET-810 |Filesize هو الحصول على أكبر أثناء إعادة استخدام نفس الملمس|إصلاح g ug|
|THREEDNET-816 |شبكة غير صحيحة أثناء التحميل OBJ|إصلاح g ug|
|THREEDNET-807 |Tهنا لا نسيج في تصدير FBX|إصلاح g ug|
|THREEDNET-815 |المواد Mمع نموذج شادر = سوف فشل غير معروف لتقديم.|إصلاح g ug|
|THREEDNET-823 |Mشبكة ultiple تعلق على نفس العقدة لا تقدم.|إصلاح g ug|
|THREEDNET-647 |Add التحكم في التحجيم I I في بائع الويب.|Ask اسأل|
|THREEDNET-646 |Add دوران التحكم UI في بائع الويب.|Ask اسأل|


## API التغييرات ##



### Added الفئة Aspose.ThreeD. hhading. exextureSمجموعة

Tله تعرض فتحات الملمس الداخلي في المواد ، من أجل الوصول إلى جميع فتحات الملمس المتاحة من مادة ، واستخدام لكل بيان:

{{< highlight "csharp" >}}
var mat = new PbrMaterial();
foreach(var textureSlot in mat)
{
    Console.WriteLine(textureSlot.SlotName);
    Console.WriteLine(textureSlot.Texture);
}
{{< /highlight >}}


### Added الفئة Aspose.ThreeD.

Rom rom 21.2 ، عندما يصل الاستخدام غير المرخص إلى تقييد الترخيص ، سيتم طرح تعليق rialEnotify restriction الترخيص ، وكيفية التقدم بطلب للحصول على ترخيص مؤقت.

You يمكن ببساطة تجاهل هذا عن طريق محاولة تحيط/قبض كتلة على ave ave/Oعملية القلم ، أو إيقاف هذا الاستثناء عن طريق:

{{< highlight "csharp" >}}
TrialException.SuppressTrialException = true;
{{< /highlight >}}

Turn هذه الرسالة قبالة لن ترفع القيود (يتم تجاهل العقد الإضافية ike إيكي من قبل المصدر/المستورد).

In الطلب للحصول على كل ميزة كاملة ، يرجى طلب رخصة مؤقتة أو شراء رخصة ميزة كاملة.

### طرق Added إلى Aspose.ThreeD.


{{< highlight "csharp" >}}
public Aspose.ThreeD.Utilities.Vector4 ReadVector4(int idx, Aspose.ThreeD.Utilities.VertexField field);
public Aspose.ThreeD.Utilities.FVector4 ReadFVector4(int idx, Aspose.ThreeD.Utilities.VertexField field);
public Aspose.ThreeD.Utilities.Vector3 ReadVector3(int idx, Aspose.ThreeD.Utilities.VertexField field);
public Aspose.ThreeD.Utilities.FVector3 ReadFVector3(int idx, Aspose.ThreeD.Utilities.VertexField field);
public Aspose.ThreeD.Utilities.Vector2 ReadVector2(int idx, Aspose.ThreeD.Utilities.VertexField field);
public Aspose.ThreeD.Utilities.FVector2 ReadFVector2(int idx, Aspose.ThreeD.Utilities.VertexField field);
public double ReadDouble(int idx, Aspose.ThreeD.Utilities.VertexField field);
public float ReadFloat(int idx, Aspose.ThreeD.Utilities.VertexField field);
{{< /highlight >}}

تسمح لك طرق These بقراءة حقل فيرتكس دون تخصيص ذاكرة إضافية ، والطريقة التقليدية للوصول إلى فيرتكس من TriMesh تولد في الواقع الكثير من الأشياء المؤقتة ، ويمكن أن توفر إمكانية الوصول إلى بصمة الذاكرة السريعة والمنخفضة.

{{< highlight "csharp" >}}
Scene s = جديد cencene (@ "test .STL") ؛
Var mesh = (Mesh)s. ooootNode. hilhildNodes [0].

// Rereate جديد erertexDeclaration ، وبالتالي فإن TriMesh قمنا ببناء في وقت لاحق سوف تستخدم هذا تخطيط الذاكرة.
فار vd = جديد VertexDeclaration() ؛
فار pos = vd. ddddFifield (VertexFieldDataType. Fecector3 ، VertexFieldS.
فار عادي = vd. ddddFifield (VertexFieldDataType. Fecector3 ، VertexFieldS. emanormal) ؛
فار الأشعة فوق البنفسجية = vd. ddddFifield (VertexFieldDataType. Fecector2 ، VertexFieldS. emaneman) ؛
// إنشاء مثال TriMesh من instance esh مثيل مع إعلان فيرتكس محدد يدويا
فار م = TriMsh. romromMsh (vd ، mesh) ؛
ل (int i = 0; i< m.VerticesCount; i++)
{
    //access each field
    var v_pos = m.ReadFVector3(i, pos);
    var v_normal = m.ReadFVector3(i, normal);
    var v_uv = m.ReadFVector3(i, uv);
    Console.WriteLine($"({v_pos}), ({v_uv}), ({v_normal})");
}
{{< /highlight >}}

### Added تنسيق ملف جديد في Aspose.ThreeD.FileFormat

{{< highlight "csharp" >}}
/// <summary>
/// Compressed Universal Scene Description
/// </summary>
public static readonly FileFormat USDZ;
{{< /highlight >}}

Aspose.3D 21.2 يمكن تحميل USDZ تنسيق الآن.


### Ixixed غير متسقة APIs:

سيتم الاحتفاظ الطبقات القديمة These لفترة من الوقت ، ويتم تقديم فئات جديدة لتحل محلها:

|**Old lass لاس** |**New lass** |
|:- |:- |
|Aspose.ThreeD. orormat. A3Dptions ptions aveOptions|Aspose.ThreeD. orormat. ptions 3dwSaveOptions|
|Aspose.ThreeD. orormat. ptions ptions ptions ptions aveOptions|Aspose.ThreeD. orormat. ptions mfSaveOptions|
|Aspose.ThreeD. orormat. ptions iscreet3Dptions ptions oadO|Aspose.ThreeD. orormat. ptions iscreet3dsLoadOالوصفات|
|Aspose.ThreeD. orormat. Discreet3Dptions ptions aveOptions|Aspose.ThreeD. orormat. ptions iscreet3dsSaveOptions|
|Aspose.ThreeD. orormat. ptions ptions ptions ptions oadO|Aspose.ThreeD. ptions ormat. ptions bxLoadO|
|Aspose.ThreeD. orormat. ptions ptions ptions ptions aveOptions|Aspose.ThreeD. orormat. ptions bxSaveOptions|
|Aspose.ThreeD. orormat. ptions ptions ptions ptions ptions oadO|Aspose.ThreeD. ptions ormat. ptions ltfLoadO|
|Aspose.ThreeD. orormat. ptions ptions ptions ptions ptions aveOptions|Aspose.ThreeD. orormat. ptions ltfSaveOptions|
|Aspose.ThreeD. orormat. Hptions ptions ptions 5SaveOptions|Aspose.ThreeD. orormat. ptions tml5SaveOptions|
|Aspose.ThreeD. orormat. ptions ptions ptions ptions oadO|Aspose.ThreeD. ptions ormat. ptions tlLoadOptions|
|Aspose.ThreeD. orormat. ptions ptions ptions ptions aveOptions|Aspose.ThreeD. orormat. ptions tlSaveOptions|
|Aspose.ThreeD. orormat. ptions 3Dptions oadO|Aspose.ThreeD. orormat. ptions 3dLoadOptions|
