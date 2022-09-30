---
title: Aspose.3D for .NET 18.1-يناير 2018
type: docs
weight: 120
url: /ar/net/aspose-3d-for-net-18-1-january-2018/
---
{{% alert color="primary" %}} 

Tصفحته تحتوي على ملاحظات الإصدار ل[Aspose.3D for .NET 18.1](https://www.nuget.org/packages/Aspose.3D/18.1.0).

{{% /alert %}} 
## **Oأكثر ements المبروفات و hangمعلقة**

|**Key**|**Sأوماري**|**Category**|
|:- |:- |:- |
|THREEDNET-331|Add كيان جديد-دعم الجذع ectالزاوي|ميزة ew ew|
|THREEDNET-323|Import an ASE وثيقة|ميزة ew ew|
|THREEDNET-327|تحويل غير صالح لملف RVM مع بدائية متعددة تحت نفس العقدة.|Bug|
|THREEDNET-325|RVM ملف مع اسطوانة مائلة غير معتمد.|Bug|
|THREEDNET-324|Cannot استيراد ملف RVM|Bug|
### **Public API و ackأكواردز hangمتوافق مع hangمعلقة**
See قائمة أي تغييرات أجريت على الجمهور API مثل إضافة أو إعادة تسميتها أو إزالتها أو إهمال الأعضاء وكذلك أي تغيير متوافق غير متخلف تم إجراؤه على Aspose.3D for .NET. If لديك مخاوف حول أي تغيير المدرجة ، يرجى رفع على[Aspose.3D دعم المنتدى](https://forum.aspose.com/c/3d/18).
#### **Member dds ASE عضو إلى Aspose.ThreeD.FileFormat الفئة**
يستخدم Tله لتحديد تنسيق الإدخال من الملف أثناء تحميل مشهد من تيار أو اسم الملف.

**C#**

{{< highlight "java" >}}

 public static readonly Aspose.ThreeD.FileFormat ASE;

{{< /highlight >}}

{{% alert color="primary" %}} 

Aspose.3D يمكن الكشف التلقائي إذا كان نوع الملف هو ASE أو غيرها من الأشكال ، وهذا عادة ما لا تكون هناك حاجة عند الاتصال Scene. Oطريقة القلم.

{{% /alert %}} 

**Sرمز وافرة**

{{< highlight "java" >}}

 Scene scene = new Scene();

scene.Open("test.ase", FileFormat.ASE);

{{< /highlight >}}
#### **Property dds enterentercene خاصية إلى Aspose.ThreeD. A3Dclass فئة حقن**
Tهو القيمة الافتراضية كاذبة ، إذا كان هذا صحيحا ، ثم Aspose.3D API سوف تحاول مركز المشهد عن طريق تحريك عقدة الجذر.

**C#**

{{< highlight "java" >}}

 Scene scene = new Scene();

scene.Open("test.rvm", new RvmLoadOptions() {CenterScene = true});

{{< /highlight >}}
#### **Adds فئة جديدة Aspose.ThreeD. nntities. ecectangularTorus**
يسمح It للمستخدم بوضع توروس مستطيلة معلمية في المشهد ، ويمكن تحويل هذا إلى شبكة/مثلث عادية أثناء حفظ المشهد إلى تنسيقات ملفات معتمدة مختلفة.

**C#**

{{< highlight "java" >}}

 /// <summary>

/// Parameterized rectangular torus.

/// </summary>

public class RectangularTorus : Primitive

{

    /// <summary>

    /// The inner radius of the rectangular torus

    /// Default value is 17

    /// </summary>

    public double InnerRadius { get; set; }

    /// <summary>

    /// The outer radius of the rectangular torus

    /// Default value is 20

    /// </summary>

    public double OuterRadius { get; set; }

    /// <summary>

    /// The height of the rectangular torus.

    /// Default value is 20

    /// </summary>

    public double Height { get; set; }

    /// <summary>

    /// The total angle of the arc, measured in radian.

    /// Default value is PI

    /// </summary>

    public double Arc { get; set; }

    /// <summary>

    /// The start angle of the arc, measured in radian.

    /// Default value is 0

    /// </summary>

    public double AngleStart { get; set; }

    /// <summary>

    /// The radial segments, default value is 10

    /// </summary>

    public int RadialSegments { get; set; }

    /// <summary>

    /// Constructor of <see cref="RectangularTorus"/>

    /// </summary>

    public RectangularTorus();

    /// <summary>

    /// Constructor of <see cref="RectangularTorus"/>

    /// </summary>

    public RectangularTorus(string name);

    /// <summary>

    /// Convert this primitive to <see cref="Mesh"/>

    /// </summary>

    /// <returns></returns>

    public Mesh ToMesh();

}

{{< /highlight >}}

**Sرمز وافرة:**

**C#**

{{< highlight "java" >}}

 RectangularTorus rt = new RectangularTorus();

rt.InnerRadius = 17;

rt.OuterRadius = 22;

rt.Height = 30;

rt.Arc = Math.PI * 0.5;

Scene scene = new Scene();

scene.RootNode.CreateChildNode(rt);

scene.Save("rtorus.obj", FileFormat.WavefrontOBJ);

{{< /highlight >}}

Tانه ولد rtorus.obj يبدو مثل:

![تودو: الصورة_البديل_نص](aspose-3d-for-net-18-1-january-2018_1.png)
#### **Uحكيم Examles**
Pالإيجار تحقق من قائمة المواضيع المساعدة المضافة أو updated في مستندات Aspose.3D Wiki:

1. [Ate reate و Read xixisting 3D cencene](/3d/ar/net/create-and-read-an-existing-3d-scene/)
1. [Create مستطيلة Torus في 3D cencene](/3d/ar/net/create-rectangular-torus-in-3d-scene/)
