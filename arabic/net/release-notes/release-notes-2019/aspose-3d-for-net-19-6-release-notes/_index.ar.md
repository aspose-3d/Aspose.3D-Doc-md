---
title: Aspose.3D for .NET 19.6 tes elease ootes
type: docs
weight: 70
url: /ar/net/aspose-3d-for-net-19-6-release-notes/
---
{{% alert color="primary" %}} 

Tصفحته تحتوي على ملاحظات الإصدار ل[Aspose.3D for .NET 19.6](https://www.nuget.org/packages/Aspose.3D/19.6.0)

{{% /alert %}} 
## **Ements proو Cمعلقة**

|**Key**|**Sأوماري**|**Category**|
|:- |:- |:- |
|THREEDNET-511|تعزيز تكوين الاسطوانة|New eature|
|THREEDNET-507|Ose نشأت بعض المواد أثناء فتح ملف RVM|Bug|
|THREEDNET-508|Tانه نظام قد تفشل في تخصيص مجموعة وصف في بعض الأحيان في renulkan renderer|Bug|
### **Public API و ackأكواردز hangمتوافق مع hangمعلقة**
See قائمة أي تغييرات أجريت على الجمهور API مثل إضافة أو إعادة تسميتها أو إزالتها أو إهمال الأعضاء وكذلك أي تغيير متوافق غير متخلف تم إجراؤه على Aspose.3D for .NET. If لديك مخاوف حول أي تغيير المدرجة ، يرجى رفع على[Aspose.3D دعم المنتدى](https://forum.aspose.com/c/3d).
#### **Property dded الملكية الجديدة ffffsetTop في الفئة Aspose.ThreeD. nntities. Cylinder**
{{< highlight "java" >}}

 /// <summary>

/// Gets or sets the vertices transformation offset of the top side.

/// </summary>

public Vector3 OffsetTop

{

    get;

    set;

}

{{< /highlight >}}
#### **Property dded الملكية الجديدة ffffsetBأوتوم في الفئة Aspose.ThreeD. nntities. Cylinder**
{{< highlight "java" >}}

 /// <summary>

/// Gets or sets the vertices transformation offset of the bottom side.

/// </summary>

public Vector3 OffsetBottom

{

    get;

    set;

}

{{< /highlight >}}

Sرمز وافرة لتوليد اسطوانة مع تخصيص ffffsetTop:

{{< highlight "java" >}}

 Scene scene = new Scene();

var fan = new Cylinder(2, 2, 10, 20, 1, false);

fan.OffsetTop = new Vector3(5, 3, 0);

scene.RootNode.CreateChildNode(fan).Transform.Translation = new Vector3(10, 0, 0);

var nonfan = new Cylinder(2, 2, 10, 20, 1, false);

scene.RootNode.CreateChildNode(nonfan);

scene.Save("test.obj", FileFormat.WavefrontOBJ);

{{< /highlight >}}

استعراض P:

![تودو: الصورة_البديل_نص](aspose-3d-for-net-19-6-release-notes_1.png)

Tترك واحد لديه**OffsetTop**تعيين إلى (5 ، 3 ، 0) ، فإنه من السهل أن نرى الغطاء العلوي قد انتقلت والجذع كله يتأثر أيضا.
#### **Property dded الملكية الجديدة enerenerateFanCylinder في الفئة Aspose.ThreeD. nntities. Cylinder**
{{< highlight "java" >}}

 /// <summary>

/// Gets or sets whether to generate the fan-style cylinder when the ThetaLength is less than 2*PI, otherwise the model will not be cut.

/// </summary>

public bool GenerateFanCylinder

{

    get;set;

}

{{< /highlight >}}

Sرمز وافرة لتوليد اسطوانة نمط مروحة واسطوانة نمط غير مروحة:

{{< highlight "java" >}}

 Scene scene = new Scene();

var fan = new Cylinder(2, 2, 10, 20, 1, false);

fan.GenerateFanCylinder = true;

fan.ThetaLength = MathUtils.ToRadian(270);

scene.RootNode.CreateChildNode(fan).Transform.Translation = new Vector3(10, 0, 0);

var nonfan = new Cylinder(2, 2, 10, 20, 1, false);

nonfan.GenerateFanCylinder = false;

nonfan.ThetaLength = MathUtils.ToRadian(270);

scene.RootNode.CreateChildNode(nonfan);

scene.Save("test.obj", FileFormat.WavefrontOBJ);

{{< /highlight >}}

استعراض P:

![تودو: الصورة_البديل_نص](aspose-3d-for-net-19-6-release-notes_2.png)

Tانه ترك اسطوانة لديها enerenerateFanCylinder = كاذبة واليمين واحد لديه enerenerateFanCylinder = صحيح.
#### **Property dded الملكية الجديدة hearhearTop في الفئة Aspose.ThreeD. nntities. Cylinder**
{{< highlight "java" >}}

 /// <summary>

/// Gets or sets of the shear transform of the top side, vector stores the (x-axis, z-axis) shear value that measured in radian, default value is (0, 0)

/// </summary>

public Vector2 ShearTop

{

    get;

    set;

}

{{< /highlight >}}
#### **Property dded عقار جديد ShearBأوتوم في الفئة Aspose.ThreeD. nntities. Cylinder**
{{< highlight "java" >}}

 /// <summary>

/// Gets or sets of the shear transform of the bottom side, vector stores the (x-axis, z-axis) shear value that measured in radian, default value is (0, 0)

/// </summary>

public Vector2 ShearBottom

{

    get;

    set;

}

{{< /highlight >}}

Sرمز وافرة لإظهار استخدام hearhearBمرتفعة (ShearTop):

{{< highlight "java" >}}

 Scene scene = new Scene();

var cylinder1 = new Cylinder(2, 2, 10, 20, 1, false);

cylinder1.ShearBottom = new Vector2(0, 0.83);// shear 47.5deg in xy plane(z-axis)

scene.RootNode.CreateChildNode(cylinder1).Transform.Translation = new Vector3(10, 0, 0);

var cylinder2 = new Cylinder(2, 2, 10, 20, 1, false);

scene.RootNode.CreateChildNode(cylinder2);

scene.Save("test.obj", FileFormat.WavefrontOBJ);

{{< /highlight >}}

استعراض P:

![تودو: الصورة_البديل_نص](aspose-3d-for-net-19-6-release-notes_3.png)

Tترك اسطوانة لديه hearhearBأوتوم إلى (0 ، 0.83) في حين أن الحق هو اسطوانة عادية.
