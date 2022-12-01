---
title: Aspose.3D for .NET 19.5 tes elease ootes
type: docs
weight: 80
url: /ar/net/aspose-3d-for-net-19-5-release-notes/
---
{{% alert color="primary" %}} 

Tصفحته تحتوي على ملاحظات الإصدار ل[Aspose.3D for .NET 19.5](https://www.nuget.org/packages/Aspose.3D/19.5.0)

{{% /alert %}} 
## **Ements proو Cمعلقة**

|**Key**|**Sأوماري**|**Category**|
|:- |:- |:- |
|THREEDNET-501|Iteمع أحدث ynynabic. tered tered|Enhancement|
|THREEDNET-505|Aانخفاض اتجاه طائرة التغيير عن طريق تحديد ما يصل العادي|Enhancement|
|THREEDNET-489|Shadow لا يعمل في renulkan renderer|Bug|
|THREEDNET-504|Draco تم إنشاؤه من STL يتم كسر الملف|Bug|
### **Public API و ackأكواردز hangمتوافق مع hangمعلقة**
See قائمة أي تغييرات أجريت على الجمهور API مثل إضافة أو إعادة تسميتها أو إزالتها أو إهمال الأعضاء وكذلك أي تغيير متوافق غير متخلف تم إجراؤه على Aspose.3D for .NET. If لديك مخاوف حول أي تغيير المدرجة ، يرجى رفع على[Aspose.3D دعم المنتدى](https://forum.aspose.com/c/3d).
#### **Added الملكية الجديدة Radius في الفئة Aspose.ThreeD. nntities. lane لين**
{{< highlight "java" >}}

 /// <summary>

/// Gets or sets the up vector of the plane, default value is (0, 1, 0), this affects the generation of the plane

/// </summary>

public Vector3 Up { get; set; }

{{< /highlight >}}

Sرمز وافرة لتحديد دائرة نصف قطرها عن طريق الممتلكات بدلا من حجة البناء:

{{< highlight "java" >}}

 Scene scene = new Scene();

scene.RootNode.CreateChildNode(new Plane() {Up = new Vector3(1, 1, 3)});

//This will generate a plane that has customized orientation

scene.Save("test.obj", FileFormat.WavefrontOBJ);

{{< /highlight >}}
#### **Added طريقة جديدة "GetConsumptionCredit" في الفئة Aspose.ThreeD.**
{{< highlight "java" >}}

 /// <summary>

/// Gets consumption credit

/// </summary>

/// <returns>consumption quantity</returns>

public static decimal GetConsumptionCredit();

{{< /highlight >}}

` `Gets الائتمان الاستهلاك من الشهر الحالي ، وتستخدم من قبل Dynabic. Mخدمة الفواتير المقننة.
