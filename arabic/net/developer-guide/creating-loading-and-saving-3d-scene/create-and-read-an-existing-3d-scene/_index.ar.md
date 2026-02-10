---
title: إنشاء وقراءة مشهد 3D موجود
type: docs
weight: 10
url: /ar/net/create-and-read-an-existing-3d-scene/
description: Aspose. يدعم 3D API إنشاء مشاهد 3D جديدة من نقطة الصفر ثم الحفظ بأي تنسيق ملف مدعوم. يمكن للمطورين أيضًا تحميل مشهد 3D موجود لأغراض التعديل أو الإضافة أو المعالجة.
---
##  **Oفيرفيو**
توضح المقالة الموضوعات التالية باستخدام مكتبة التلاعب بتنسيقات الملفات C# 3D.
- إنشاء مشهد 3D فارغ بـ C# من الصفر
- قراءة أو تحميل مشهد 3D الحالي بـ C#
- احفظ مشهد 3D بتنسيقات 3D المدعومة باستخدام C#
- العمل مع خصائص مشهد 3D في C#

##  **قم بإنشاء مشهد 3D فارغ ووفر في تنسيقات الملفات 3D المدعومة**
Aspose. يدعم 3D API إنشاء مشاهد 3D جديدة من نقطة الصفر ثم الحفظ بأي تنسيق ملف مدعوم. يمكن للمطورين أيضًا تحميل مشهد 3D موجود لأغراض التعديل أو الإضافة أو المعالجة.

###  **إنشاء مستند مشهد 3D**
يرجى اتباع هذه الخطوات في C# لإنشاء مستند مشهد 3D باستخدام Aspose.3D APIs:

1. أنشئ مثيل لفئة [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) التي تمثل مستند مشهد 3D.
1. قم بإنشاء مستند مشهد 3D عن طريق استدعاء طريقة [`Save`](https://reference.aspose.com/3d/net/aspose.threed/scene/methods/save) لكائن فئة المشهد.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET

// Create an object of the Scene class
Scene scene = new Scene();
// Save 3D scene document
scene.Save("document.fbx");

{{< /highlight >}}

##  **قراءة مشهد 3D**
باستخدام Aspose.3D API ، يمكن للمطورين تحميل جميع مستندات 3D المدعومة. تسمح المنشئات المتاحة لفئة `Scene` بذلك وتقبل سلسلة مسار ملف صالحة. تنسيقات الملفات المقروءة المدعومة هي كما يلي:

1. FBX 7.5 (ASCII ، ثنائي)
1. FBX 7.4 (ASCII ، ثنائي)
1. FBX 7.3 (ASCII ، ثنائي)
1. FBX 7.2 (ASCII ، ثنائي)
1. FBX 6.1 (ASCII ، ثنائي)
1. STL (ASCII, Binary)
1. WavefrontOBJ
1. Discreet3DS
1. Universal3D
1. Collada
1. glTF (ASCII, Binary)
1. مايا (أسكي ، ثنائي)
1. OpenUSD (USD ، USDZ)
1. خلاط
1. DXF
1. PLY (ASCII, Binary)
1. X (ASCI I ، inary inary)
1. Draco
1. 3MF
1. RVM (Text, Binary)
1. ASE

تكتشف منشئات فئة `Scene` تنسيق المستند 3D داخليًا.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// The path to the documents directory.

// Initialize a Scene class object
Scene scene = new Scene();
// Load an existing 3D document
scene.Open("document.fbx");


{{< /highlight >}}

##  **العمل مع خصائص المشهد 3D**
Aspose.3D API يتيح لك قراءة خصائص المشهد 3D باستخدام عقد الطفل للمشهد. توضح عينة رمز C# التالية استخدام هذه الميزة.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
Scene scene = Scene.FromFile("EmbeddedTexture.fbx");
Material material = scene.RootNode.ChildNodes[0].Material;
PropertyCollection props = material.Properties;
//List all properties using foreach
foreach (var prop in props)
{
    Console.WriteLine("{0} = {1}", prop.Name, prop.Value);
}
//or using ordinal for loop
for (int i = 0; i < props.Count; i++)
{
    var prop = props[i];
    Console.WriteLine("{0} = {1}", prop.Name, prop.Value);
}
//Get property value by name
var diffuse = props["Diffuse"];
Console.WriteLine(diffuse);
//modify property value by name
props["Diffuse"] = new Vector3(1, 0, 1);
//Get property instance by name
Property pdiffuse = props.FindProperty("Diffuse");
Console.WriteLine(pdiffuse);
//Since Property is also inherited from A3DObject
//It's possible to get the property of the property
Console.WriteLine("Property flags = {0}", pdiffuse.GetProperty("flags"));
//and some properties that only defined in FBX file:
Console.WriteLine("Label = {0}", pdiffuse.GetProperty("label"));
Console.WriteLine("Type Name = {0}", pdiffuse.GetProperty("typeName"));
//so traversal on property's property is possible
foreach (var pp in pdiffuse.Properties)
{
    Console.WriteLine("Diffuse.{0} = {1}", pp.Name, pp.Value);
}

{{< /highlight >}}
