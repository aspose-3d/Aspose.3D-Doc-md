---
title: دعم خصائص IFC
type: docs
linkTitle: دعم خصائص IFC
description: توضح صفحة الوثائق هذه كيفية قراءة الخصائص من ملف IFC باستخدام Aspose.3D for .NET.
weight: 14
i18n_hash: 28432129a06817407d71b2b6ec86d81d
---

## نظرة عامة

دعم خصائص IFC هو ميزة في Aspose.3D تتيح للمطورين قراءة مجموعات الخصائص وكميات العناصر المعرفة في ملفات IFC. تُخزن هذه الخصائص في كيانات `IFCPROPERTYSET` و `IFCELEMENTQUANTITY` ويمكن الوصول إليها عبر طريقة `A3DObject.GetProperty`.

## ما هو دعم خصائص IFC؟

في مخطط IFC، يمكن أن تحتوي عناصر المبنى على مجموعات خصائص مرتبطة (`IFCPROPERTYSET`) وكميات عناصر (`IFCELEMENTQUANTITY`). تقوم Aspose.3D بربط هذه إلى واجهة خصائص عامة، وتعرضها عبر `A3DObject.GetProperty(string propertyName)`. يتيح ذلك استرجاع قيم مثل تصنيف الحريق، معامل انتقال الحرارة، أو كميات المواد مباشرةً من النموذج ثلاثي الأبعاد.

## لماذا نستخدم دعم خصائص IFC؟

* الوصول إلى بيانات دلالية غنية دون الحاجة إلى تحليل ملف IFC يدوياً.  
* تمكين عمليات ما بعد المعالجة مثل تقدير التكلفة، التحقق من الامتثال، أو تصدير البيانات.  
* دمج المعلومات الهندسية وغير الهندسية في سير عمل واحد.

## دعم Aspose.3D

يوضح المثال التالي بلغة C# كيفية تحميل ملف IFC وقراءة خاصية:

```csharp
using Aspose.ThreeD;

var scene = Scene.FromFile("sample.ifc");

// ابحث عن عنصر محدد، على سبيل المثال جدار
var wallNode = scene.RootNode.Children.FirstOrDefault(n => n.Name == "Wall_123");

// استرجاع قيمة الخاصية
if (wallNode != null)
{
    // اسم الخاصية كما هو معرف في ملف IFC
    var fireRating = wallNode.GetProperty("ifc:FireRating");
    Console.WriteLine($"Fire Rating: {fireRating}");

    // مثال على كمية العنصر
    var volume = wallNode.GetProperty("ifc:GrossVolume");
    Console.WriteLine($"Gross Volume: {volume}");
}
```

### ملاحظات

* أسماء الخصائص المعرفة في ملف IFC تُسبق بـ `ifc:` لتجنب التعارض مع الخصائص الأصلية.  
* أسماء الخصائص حساسة لحالة الأحرف ويجب أن تطابق الأسماء المعرفة في ملف IFC.  
* `GetProperty` تُعيد كائنًا من النوع `object`؛ يلزم تحويله إلى النوع المناسب (مثل `double` أو `string`) حسب الحاجة.  
* يوضح هذا المثال استرجاع الخصائص من `Node`؛ ومع ذلك، يمكن لأي فئة مشتقة من `A3DObject` استخدام `GetProperty`.  
* إذا لم تكن الخاصية موجودة، تُعيد `GetProperty` القيمة `null`.

## مراجع

* [Link to official Aspose.3D IFC documentation](/3d/net/supported-file-formats/ifc)  
* رابط إلى [`Aspose.ThreeD.A3DObject`](https://reference.aspose.com/3d/net/aspose.threed/a3dobject/)  
* مواصفات IFC لـ `IFCPROPERTYSET` و `IFCELEMENTQUANTITY`