---
title: Aspose.3D for .NET 21.3 tes elease ootes
type: docs
weight: 10
url: /ar/net/aspose-3d-for-net-21-3-release-notes/
---
{{% alert color="primary" %}}

Tصفحته تحتوي على معلومات ملاحظات الافراج عن Aspose.3D for .NET 21.3.

{{% /alert %}}
## **Ements proو Cمعلقة**

|**Key**|**Sأوماري**|**Category**|
|:- |:- |:- |
|THREEDNET-847 |Add نقطة دعم سحابة في glb|ميزة ew ew|
|THREEDNET-830 |Provide شبكة منخفضة المستوى API لبائع الويب.|حركة بلا حدود|
|THREEDNET-838 |Export 2.5D opالتصوير البصري مع اللون إلى ملف|حركة بلا حدود|
|THREEDNET-849 |Add بايت [4] دعم في glTF التصدير|حركة بلا حدود|
|THREEDNET-832 |Gmplement gizmos للضوء في بائع الويب|حركة بلا حدود|
|THREEDNET-833 |Implement gizmo للكاميرا في بائع الويب|حركة بلا حدود|
|THREEDNET-842 |Add عامل Uparتحليل الدعم في FBX|حركة بلا حدود|
|THREEDNET-852 |إعادة اختبار العمارة renderer ntity لبائع الويب|Ask اسأل|
|THREEDNET-836 |Pتثبيت أسماء فئة خيار حفظ/تحميل.|Ask اسأل|
|THREEDNET-858 |لم يتم تقديم ملف ome ome obj بالكامل في بائع الويب.|إصلاح g ug|
|THREEDNET-859 |لا يمكن استيراد الملفات X مع هيكل الرسوم المتحركة غير القياسية.|إصلاح g ug|
|THREEDNET-861 |Cannot استيراد ملفات X مع بيانات FVF محددة|إصلاح g ug|
|THREEDNET-860 |Cannot استيراد ملفات X مع مواد متعددة تعلق على شبكة واحدة|إصلاح g ug|
|THREEDNET-839 |FBX لا يتم دعم الملف مع ConstraintParent.|إصلاح g ug|
|THREEDNET-841 |Some القديم FBX الملفات تحتوي على قسم Shape تحت Model غير معتمدة.|إصلاح g ug|
|THREEDNET-840 |ASCII FBX File مع failed ileId سوف فشلت في الاستيراد.|إصلاح g ug|
|THREEDNET-844 |API هو رمي عدم التسليم أثناء وضع رخصة سارية المفعول في .NET Core|إصلاح g ug|
|THREEDNET-843 |API لا يضع استثناء رمي رخصة سارية المفعول في .NET مشروع خام C|إصلاح g ug|
|THREEDNET-848 |لا يمكن تصدير سحابة نقطة ome ome إلى جمهورية الكونغو الديمقراطية|إصلاح g ug|
|THREEDNET-854 |Aspose.3D تحطمت عند استيراد بعض ملفات كولادا مع تعريفات مادية غير صحيحة.|إصلاح g ug|


## API التغييرات ##


Tنسخته هي أساسا نسخة إصلاح الأخطاء ، الثابتة مجموعة من الأخطاء ، وتحسين مجموعة من التوافق ل FBX ، Collada ، DirectX الملفات X.


ملاحظة عدد قليل من التغييرات الطفيفة API.

### Added نوع بيانات جديد في الفئة Aspose.ThreeD. tilitulties. VertexFieldDataType:

{{< highlight "java" >}}

    /// <summary>
    /// Type of byte[4], can be used to represent color with less memory consumption.
    /// </summary>
    public static Aspose.ThreeD.Utilities.VertexFieldDataType ByteVector4;

{{< /highlight >}}

سيتم ترميز eometry كما عدد صحيح 4 بايت مع نوع VertexFieldDataType.ByteVector4.

Tله يمكن أن تقلل من الملف النهائي ولدت إلى حد كبير في glTF/glb التي تستخدم لون فيرتكس ، مفيدة جدا لترميز الغيوم نقطة.

And من هذا الإصدار ، ويدعم Aspose.ThreeD. nntities. PointCبصوت عال في glTF/glb فتح وحفظ.



### أعضاء Added إلى الفئة Aspose.ThreeD.


{{< highlight "java" >}}


    /// <summary>
    /// The size of the bounding box
    /// </summary>
    Aspose.ThreeD.Utilities.Vector3 Size{ get;}

    /// <summary>
    /// The center of the bounding box.
    /// </summary>
    Aspose.ThreeD.Utilities.Vector3 Center{ get;}

{{< /highlight >}}

Now أنه من الأسهل للحصول على حجم ومركز صندوق الحدود ، وهذه الخصائص لا معنى لها إلا عندما يكون الثور oundفي نهاية المطاف.

