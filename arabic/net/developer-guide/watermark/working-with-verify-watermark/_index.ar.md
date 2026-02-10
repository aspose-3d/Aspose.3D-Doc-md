---
title: العمل مع التحقق من العلامة المائية
type: docs
weight: 170
url: /ar/net/working-with-verify-watermark/
---

{{% alert color="primary" %}}

باستخدام واجهة برمجة تطبيقات Aspose.3D لـ .NET، يمكن للمطورين بسهولة إضافة التحقق من العلامة المائية المخفية إلى ملفات ثلاثية الأبعاد أثناء الحفظ في أي تنسيق ملف إخراج مدعوم.

{{% /alert %}}
# **إنشاء مشهد ثلاثي الأبعاد**
أولاً، تحتاج إلى إنشاء مشهد ثلاثي الأبعاد من ملف ثلاثي الأبعاد. يوضح المقتطف البرمجي التالي كيفية استخدام هذه الوظيفة:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
string file = "template.3ds";
Scene scene = Scene.FromFile(file);
{{< /highlight >}}

# **فك ترميز العلامة المائية**
تستخدم واجهة برمجة تطبيقات Aspose.3D لـ .NET طريقة `DecodeWatermark` لتأكيد العلامة المائية لملف ثلاثي الأبعاد بعد إدخال كلمة المرور. يوضح المقتطف البرمجي التالي كيفية استخدام هذه الوظيفة:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
string text = null;
try
{
    scene.RootNode.Accept((Node node) =>
    {
        var mesh = node.GetEntity<Mesh>();
        if (mesh != null)
        {
            text = Watermark.DecodeWatermark(mesh, "1234");
            if (text != null)
                return false;
        }
        return true;
    });
}
catch (UnauthorizedAccessException)
{
    return "Password error";
}
return text;
{{< /highlight >}}

# **تأكيد المستند**
بالنسبة للنتيجة المرجعة، إذا كانت النتيجة المرجعة فارغة، فهذا يعني عدم وجود علامة مائية مضافة إلى المستند ثلاثي الأبعاد. إذا أرجعت معلومات نصية، فهي العلامة المائية لملف ثلاثي الأبعاد. إذا تم إدخال كلمة المرور بشكل غير صحيح، سيتم إرجاع رسالة خطأ.