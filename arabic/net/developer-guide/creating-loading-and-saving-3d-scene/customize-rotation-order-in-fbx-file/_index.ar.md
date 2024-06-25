---
title: تخصيص طلب تدوير في ملف FBX
type: docs
weight: 10
url: /ar/net/customize-rotation-order-in-fbx-file
description: باستخدام Aspose.3D for .NET ، يمكن للمطورين تحديد خصائص FBX الأصلية مثل RotationOrder.
---
{{% alert color="primary" %}}

Using [Aspose.3D for .NET](https://products.aspose.com/3d/net/), Sometimes, developers require fine control over format-specific features, such as changing the `RotationOrder` in the FBX exporter. While there might not be a public API directly exposing this functionality, Aspose.3D for .NET provides ways to achieve such customizations through its flexible architecture.
{{% /alert %}}



إليك كيف يمكنك التعامل مع هذا بـ Aspose.3D:

{{% highlight "csharp" %}}

var rvm = Scene.FromFile(@"F1234.rvm");
rvm.RootNode.Accept((Node node) =>
{
    node.SetProperty("RotationOrder", 1); //set a custom property, exporter will match this to FBX's property.
    return true; //continue to traverse on other nodes 
});

rvm.Save(@"test.fbx");

{{% /highlight %}}

في هذا المثال:

1. أنشئ مشهدًا من ملف RVM.
1. زيارة كل عقدة في المشهد.
1. تعيين خاصية مخصصة: تُستخدم طريقة setproerty لتعيين خاصية `RotationOrder` ، مما يوضح كيف يمكن الاستفادة من الآليات الداخلية للتحكم في الميزات الخاصة بالتنسيق التي لا يعرضها الجمهور مباشرة API.
1. حفظ المشهد: تم حفظ المشهد مع `RotationOrder` المخصص.

باستخدام هذه التقنيات ، يسمح Aspose.3D للمطورين بضبط الميزات المحددة للتنسيقات 3D والتحكم فيها ، مما يضمن تلبية المتطلبات التفصيلية والدقيقة في مختلف تطبيقات 3D.