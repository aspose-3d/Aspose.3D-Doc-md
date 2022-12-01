---
title: Aspose.3D for .NET 19.4 tes elease ootes
type: docs
weight: 90
url: /ar/net/aspose-3d-for-net-19-4-release-notes/
---
{{% alert color="primary" %}} 

Tصفحته تحتوي على ملاحظات الإصدار ل[Aspose.3D for .NET 19.4](https://www.nuget.org/packages/Aspose.3D/19.4.0)

{{% /alert %}} 
## **Ements proو Cمعلقة**

|**Key**|**Sأوماري**|**Category**|
|:- |:- |:- |
|THREEDNET-471|Xath مثل طرق معالجة الكائن|ميزة ew ew|
|THREEDNET-483|Upupport لتنسيق VRML|ميزة ew ew|
|THREEDNET-493|دعم rendded renulkan في .NET إصدار خام C|ميزة ew ew|
|THREEDNET-496|FB757500Binary inary xport ororroution sسو|Bug|
### **Public API و ackأكواردز hangمتوافق مع hangمعلقة**
See قائمة أي تغييرات أجريت على الجمهور API مثل إضافة أو إعادة تسميتها أو إزالتها أو إهمال الأعضاء وكذلك أي تغيير متوافق غير متخلف تم إجراؤه على Aspose.3D for .NET. If لديك مخاوف حول أي تغيير المدرجة ، يرجى رفع على[Aspose.3D دعم المنتدى](https://forum.aspose.com/c/3d).
#### **Added عقار جديد Radius في الفئة Aspose.ThreeD. nntities. Sphere**
{{< highlight "java" >}}

 /// <summary>

/// Gets or sets the radius of the sphere.

/// </summary>

public double Radius { get; set; }

{{< /highlight >}}

Sرمز وافرة لتحديد دائرة نصف قطرها عن طريق الممتلكات بدلا من حجة البناء:

{{< highlight "java" >}}

 Scene scene = new Scene();

scene.RootNode.CreateChildNode(new Sphere() {Radius = 10});

scene.Save("sphere.obj", FileFormat.WavefrontOBJ);

{{< /highlight >}}
#### **Added تنسيق ملف جديد VRML في الفئة Aspose.ThreeD.FileFormat و Aspose.ThreeD.**
{{< highlight "java" >}}

 /// <summary>

/// The Virtual Reality Modeling Language

/// </summary>

public static readonly FileFormat VRML;

{{< /highlight >}}

Aspose.3D يمكن الكشف التلقائي VRML تنسيق ، وبالتالي فإن FileFormat عادة ما يتم تجاهلها في طريقة القلم O. Sرمز وافرة:

{{< highlight "java" >}}

 Scene scene = new Scene();

scene.Open("test.wrl");

{{< /highlight >}}
