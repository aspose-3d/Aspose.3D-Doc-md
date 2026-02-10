---
title: العمل مع العلامة المائية
type: docs
weight: 160
url: /ar/net/working-with-watermark/
---

{{% alert color="primary" %}}

باستخدام واجهة برمجة تطبيقات Aspose.3D لـ .NET، يمكن للمطورين بسهولة إضافة علامات مائية غير مرئية إلى ملفات ثلاثية الأبعاد أثناء الحفظ بتنسيق ملف إخراج مدعوم.

{{% /alert %}}
# **إنشاء مشهد ثلاثي الأبعاد**
أولاً، تحتاج إلى إنشاء مشهد ثلاثي الأبعاد من ملف ثلاثي الأبعاد. يوضح المقتطف البرمجي التالي كيفية استخدام هذه الوظيفة:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
string file = "template.3ds";
Scene scene = Scene.FromFile(file);
{{< /highlight >}}

# **ترميز العلامة المائية**
تضيف واجهة برمجة تطبيقات Aspose.3D لـ .NET معلومات نص العلامة المائية وكلمة مرور العلامة المائية إلى ملفات ثلاثية الأبعاد من خلال طريقة ``EncodeWatermark``. يوضح المقتطف البرمجي التالي كيفية استخدام هذه الوظيفة:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
var numMeshes = 0;
scene.RootNode.Accept((Node node) =>
{
    var mesh = node.GetEntity<Mesh>();
    if (mesh != null)
    {
        numMeshes++;
        mesh = Watermark.EncodeWatermark(mesh, "HelloWorld", "1234");
        if (mesh != null)
        {
            node.Entity = mesh;
        }
    }
    return true;
});
{{< /highlight >}}

# **حفظ المستند**
يمكنك الحفظ بأي تنسيق ملف ثلاثي الأبعاد تريده. يوضح المقتطف البرمجي التالي كيفية استخدام هذه الوظيفة:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
string output = "output.fbx";
scene.Save(output, FileFormat.FBX7400ASCII);
{{< /highlight >}}