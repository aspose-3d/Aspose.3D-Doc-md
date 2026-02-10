---
title: دعم مجموعة IFC
type: docs
linkTitle: دعم مجموعة IFC
description: توثّق هذه الصفحة كيفية قراءة التسلسل الهرمي الدلالي من ملف IFC باستخدام Aspose.3D for .NET.
weight: 14
i18n_hash: 34bf3dc260d3bf202703b6f70981f703
---

# دعم مجموعة IFC

## نظرة عامة

مجموعة IFC هي ميزة تم تقديمها حديثًا في Aspose.3D تمكّن المطورين من العمل مع المجموعات الدلالية المعرفة في ملفات IFC. على عكس التسلسل الهرمي الهندسي التقليدي، توفر مجموعة IFC طريقة لتمثيل عناصر المبنى بتجميع ذي معنى، مما يسمح باستخراج البيانات ومعالجتها بشكل أغنى.

## ما هي مجموعة IFC؟

في تنسيق IFC (Industry Foundation Classes)، تُستخدم المجموعات لإنشاء تسلسل هرمي قائم على الدلالة يجمع الكيانات المرتبطة (مثل الجدران، الأبواب) تحت معرف مشترك. تعرض Aspose.3D هذه المجموعات من خلال فئة [`Group`](https://reference.aspose.com/3d/net/aspose.threed/group/) ، مما يتيح الوصول إلى اسم المجموعة، المعلومات الدلالية، والعقد الفرعية.

## لماذا نستخدم مجموعة IFC؟

إضافة مجموعة IFC تضيف سياقًا دلاليًا إلى مخطط المشهد الهندسي البحت، مما يجعل من السهل الاستعلام، الترشيح، ومعالجة عناصر المبنى بناءً على معناها الحقيقي. يبسط ذلك مهام مثل استخراج مكونات المبنى المحددة، تطبيق تجاوزات المواد، أو إنشاء تقارير مفصلة.

## دعم Aspose.3D

توفر Aspose.3D دعمًا كاملاً لمجموعة IFC في واجهة برمجة التطبيقات .NET. توضح الأقسام التالية كيفية تمكين والعمل مع مجموعات IFC.

### الوصول إلى معلومات المجموعة

```csharp
// تحميل ملف IFC
var scene = Aspose.ThreeD.Scene.FromFile("model.ifc");
// التكرار عبر المجموعات
foreach(Group group in scene2.Library.Where(obj => obj is Group))
{
    Console.WriteLine($"Group Name: {group.Name}");
    Console.WriteLine($" Sub Groups: {group.Groups.Count}");
    Console.WriteLine($" Associated Nodes: {group.Nodes.Count}");
}
```

## مثال على الشيفرة

المثال التالي من البداية إلى النهاية يقوم بتحميل ملف IFC، ويطبع التسلسل الهرمي الدلالي:

```csharp
using Aspose.ThreeD;

var scene = Scene.FromFile("sample.ifc");
scene.Open("sample.ifc", loadOptions);

void PrintGroup(Group group, string indent = "")
{
    foreach (var child in group.Groups)
    {
        Console.WriteLine($"{indent}{child.Name}");
        PrintGroup(child, indent + "  ");
    }
}

foreach(Group group in scene2.Library.Where(obj => obj is Group))
{
    PrintGroup(group);
}
```

## المراجع

* [رابط إلى وثائق Aspose.3D الرسمية لـ IFC](/3d/net/supported-file-formats/ifc)
* [رابط إلى `Aspose.ThreeD.Group`](https://reference.aspose.com/3d/net/aspose.threed/group/)
* [رابط إلى مواصفات IFC](https://technical.buildingsmart.org/standards/ifc/ifc-schema-specifications/)