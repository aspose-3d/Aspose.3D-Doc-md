---
title: نظام محور مخصص لتنسيق obj
linktitle: تخصيص نظام محور أثناء تصدير المشهد إلى تنسيق OBJ
type: docs
weight: 70
url: /ar/net/customize-axis-system-for-obj-format
description: ليس لدى OBJ نظام إحداثيات افتراضي ، يمكننا تحديد نظام محور له يدويًا.
---
{{% alert color="primary" %}} 

لا تلتزم ملفات Wavefront OBJ بنظام إحداثيات قياسي ؛ بدلاً من ذلك ، يعالج المستورد التفسير عادةً. ومع ذلك ، يوفر [Aspose.3D for .NET](https://products.aspose.com/3d/net/) المرونة لتحديد نظام محور يدويًا للملفات OBJ. وهذا يشمل تحديد المحاور الأمامية والأمامية وكذلك الاختيار بين أنظمة الإحداثيات باليد اليسرى واليمنى. Aspose. سيتعامل 3D تلقائيًا مع تحويل نظام الإحداثيات ، مما يضمن الاتساق والدقة في طرازات 3D.


{{% /alert %}} 
##  **تحديد نظام محور للملفات OBJ في Aspose.3D**

إليك كيفية ضبط نظام المحور يدويًا عند العمل مع ملفات OBJ في Aspose.3D:

{{< highlight "csharp" >}}
//construct a right-handed axis system with +y as up and -z as front
Axis up = Axis.YAxis;
Axis front = Axis.NegativeZAxis;
AxisSystem axisSystem = new AxisSystem(CoordinateSystem.RightHanded, up, front);

ObjSaveOptions opt = new ObjSaveOptions();
//use the custom axis system to flip coordinate
opt.AxisSystem = axisSystem;
//set this to true, will convert mesh's position/normal from source axis system to custom axis system
//source axis system is defined by scene.AssetInfo.CoordinateSystem, scene.AssetInfo.UpVector, scene.AssetInfo.FrontVector
opt.FlipCoordinateSystem = true;

 // initialize a new 3D scene from existing file

var scene = Scene.FromFile("input.dae");

// Save the scene with customized axis system
s.Save("output.obj", opt);

{{< /highlight >}}

باستخدام تكوين نظام محور Aspose.3D للملفات OBJ ، يمكنك تحقيق نتائج استيراد متسقة ودقيقة بغض النظر عن نظام الإحداثيات الأصلي المستخدم في ملف OBJ. تعزز هذه الميزة المرونة والتحكم ، مما يسهل الدمج والعمل مع ملفات OBJ بسير عمل مختلف بقيمة 3D.

##  **Resources**

1. [البرنامج التعليمي عبر الإنترنت](https://products.aspose.com/3d/tutorial/)
2. [أكسيسيستم](https://reference.aspose.com/3d/net/aspose.threed/axissystem/)