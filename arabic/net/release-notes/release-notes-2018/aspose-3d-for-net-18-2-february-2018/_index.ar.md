---
title: Aspose.3D for .NET 18.2-فبراير 2018
type: docs
weight: 110
url: /ar/net/aspose-3d-for-net-18-2-february-2018/
---
{{% alert color="primary" %}} 

Tصفحته تحتوي على ملاحظات الإصدار ل[Aspose.3D for .NET 18.2](https://www.nuget.org/packages/Aspose.3d/18.2.0).

{{% /alert %}} 
## **Oأكثر ements المبروفات و hangمعلقة**

|**Key**|**Sأوماري**|**Category**|
|:- |:- |:- |
|THREEDNET-335|Mmplement إضافة الأقواس arإلى hanorphهانيل|ميزة ew ew|
|THREEDNET-348|Add دعم الهيكل العظمي/نقل الرسوم المتحركة التصدير|ميزة ew ew|
|THREEDNET-332|دعم dd dd curve curve curve curve curve منحنى|ميزة ew ew|
|THREEDNET-333|دعم dd dd لسطح NUdd dd dd|ميزة ew ew|
|THREEDNET-338|دعم dd dd من Pre/Post tation|ميزة ew ew|
|THREEDNET-351|Cannot تجعل الشفافية على PNG صورة المشهد|Enhancement|
|THREEDNET-334|Outplace FBX-حدث خطأ مؤشر بدن|Bug|
### **Public API و ackأكواردز hangمتوافق مع hangمعلقة**
See قائمة أي تغييرات أجريت على الجمهور API مثل إضافة أو إعادة تسميتها أو إزالتها أو إهمال الأعضاء وكذلك أي تغيير متوافق غير متخلف تم إجراؤه على Aspose.3D for .NET. If لديك مخاوف حول أي تغيير المدرجة ، يرجى رفع على[Aspose.3D دعم المنتدى](https://forum.aspose.com/c/3d/18).
#### **أعضاء dds Aإلى Aspose.ThreeD. eeformers. Bفئة واحدة**
**C#**

{{< highlight "java" >}}

 /// <summary>

/// Gets the weight for control point specified by index

/// </summary>

/// <param name="index">Control point's index</param>

/// <returns>the weight at specified index, or 0 if the index is invalid</returns>

public double GetWeight(int index)

/// <summary>

/// Sets the weight for control point specified by index

/// </summary>

/// <param name="index">Control point's index</param>

/// <param name="weight">New weight</param>

public void SetWeight(int index, double weight)

/// <summary>

/// Gets the count of weight, this is automatically extended by <see cref="SetWeight"/>

/// </summary>

int WeightCount{ get;}

/// <summary>

/// Gets or sets the transform matrix of the bone.

/// </summary>

Aspose.ThreeD.Utilities.Matrix4 BoneTransform{ get;set;}

{{< /highlight >}}
#### **أعضاء Adds إلى Aspose.ThreeD.**
**C#**

{{< highlight "java" >}}

 /// <summary>

/// Gets the weight for the specified target, if the target is not belongs to this channel, default value 0 is returned. 

/// </summary>

/// <param name="target"></param>

/// <returns></returns>

public double GetWeight(Aspose.ThreeD.Entities.Geometry target)

/// <summary>

/// Sets the weight for the specified target, default value is 1, range should between 0~1

/// </summary>

/// <param name="target"></param>

/// <param name="weight"></param>

public void SetWeight(Aspose.ThreeD.Entities.Geometry target, double weight)

{{< /highlight >}}
#### **أعضاء Adds في الفئة Aspose.ThreeD. nntities. ururbsCurve**
**C#**

{{< highlight "java" >}}

 /// <summary>

/// Evaluate the nurbs curve

/// </summary>

/// <param name="steps">The evaluation frequency between two neighbor knots, default value is 20</param>

/// <returns>Points in the curve</returns>

public Aspose.ThreeD.Utilities.Vector4[]Evaluate(double delta)

/// <summary>

/// Evaluate the curve's point at specified position

/// </summary>

/// <param name="u">The position in the curve, between 0 and 1</param>

/// <returns></returns>

public Aspose.ThreeD.Utilities.Vector4 EvaluateAt(double u)

{{< /highlight >}}

**Sرمز وافرة:**

**C#**

{{< highlight "java" >}}

 public static void Main(string[]args)

{

    NurbsCurve curve = new NurbsCurve();

    curve.ControlPoints.AddRange(new Vector4[]{

        new Vector4(-28.0118217468262, 53.0359077453613, 0, 1),

        new Vector4(8.95330429077148, 64.7735290527344, 0, 1),

        new Vector4(35.7778739929199, 42.424259185791, 0, 1),

        new Vector4(24.8725852966309, -4.86993026733398, 0, 1),

        new Vector4(-35.7778739929199, -34.192684173584, 0, 1),

        new Vector4(-18.6066780090332, -57.1458396911621, 0, 1),

        new Vector4(17.733715057373, -64.7735290527344, 0, 1)

    });

    curve.KnotVectors.AddRange(new double[]{0, 0, 0, 0, 0.25, 0.5, 0.75, 1, 1, 1, 1});

    foreach (var pt in curve.Evaluate())

    {

        Console.WriteLine(pt);

    }

}

{{< /highlight >}}
#### **أعضاء Adds إلى Aspose.ThreeD. nntities. ururbsCurve الفئة**
**C#**

{{< highlight "java" >}}

 /// <summary>

/// Convert the nurbs surface to the mesh

/// </summary>

/// <returns></returns>

public Aspose.ThreeD.Entities.Mesh ToMesh()

{{< /highlight >}}

{{% alert color="primary" %}} 

بما في ذلك الإصدار الأخير 18.2 من Aspose.3D for .NET ، فإن سطح NUBS أصبح الآن قادرًا.

{{% /alert %}} {{% alert color="primary" %}} 

The NUsurface surface السطح الذي يحتوي على اتجاه U/V الدوري غير معتمد بعد ، سيتم دعمه في الإصدارات المستقبلية.

{{% /alert %}}
#### **أعضاء dds Aإلى Aspose.ThreeD. فئة ransform ran**
تحتوي ملفات ome ome FBX على قيمة دوران غير صفر قبل/بعد للعقد ، هذه الخصائص اثنين يعرضها للمستخدم وتسمح لك بالتلاعب بها.

**C#**

{{< highlight "java" >}}

 /// <summary>

/// Gets or sets the pre-rotation represented in degree

/// </summary>

Aspose.ThreeD.Utilities.Vector3 PreRotation{ get;set;}

/// <summary>

/// Gets or sets the post-rotation represented in degree

/// </summary>

Aspose.ThreeD.Utilities.Vector3 PostRotation{ get;set;}

{{< /highlight >}}
#### **أعضاء Adds إلى Aspose.ThreeD.**
**C#**

{{< highlight "java" >}}

 /// <summary>

/// Convert a number from radian to degree

/// </summary>

/// <param name="x">The x component in radian value.</param>

/// <param name="y">The y component in radian value.</param>

/// <param name="z">The z component in radian value.</param>

/// <returns>The degree value.</returns>

public static Aspose.ThreeD.Utilities.Vector3 ToDegree(double x, double y, double z)

/// <summary>

/// Convert a vector from degree to radian

/// </summary>

/// <param name="x">The x component in degree value.</param>

/// <param name="y">The y component in degree value.</param>

/// <param name="z">The z component in degree value.</param>

/// <returns>The radian value.</returns>

public static Aspose.ThreeD.Utilities.Vector3 ToRadian(double x, double y, double z)

{{< /highlight >}}

Tانه مثال التعليمات البرمجية القديمة:

**C#**

{{< highlight "java" >}}

 MathUtils.ToDegree(new Vector3(x, y, z));

MathUtils.ToRadian(new Vector3(x, y, z));

{{< /highlight >}}

يمكن الآن تبسيط It على النحو التالي:

**C#**

{{< highlight "java" >}}

 MathUtils.ToDegree(x, y, z);

MathUtils.ToRadian(x, y, z);

{{< /highlight >}}

{{% alert color="primary" %}} 

Tانه بعد التغييرات يجب أن تجلب أي تغييرات رمز على جانب المستخدم ، لكنها مطلوبة لإصدار جافا للحفاظ على الاتساق.

{{% /alert %}} 
#### **Member تحديث في Aspose.ThreeD. orormat. GLptions ptions ptions**
**تعريف ld ld**

{{< highlight "java" >}}

 System.Func<Aspose.ThreeD.Shading.Material, Aspose.ThreeD.Shading.Material> MaterialConverter{ get;set;}

{{< /highlight >}}

**تعريف ew**

{{< highlight "java" >}}

 //New definition

Aspose.ThreeD.Formats.MaterialConverter MaterialConverter{ get;set;}

{{< /highlight >}}

Tانه تعريف MaterialConverter لديه نفس التوقيع على Fالقديمة unc<Material, Material>:

**C#**

{{< highlight "java" >}}

 /// <summary>

/// Custom converter to convert the geometry's original material to GLTF's PBR material.

/// </summary>

/// <param name="mat">Old material instance</param>

/// <returns>New material instance</returns>

public delegate Material MaterialConverter(Material mat);

{{< /highlight >}}
#### **Adds فئة جديدة Aspose.ThreeD. nntities. erertexEleالقابل Vector4**
Tفئته هي فئة قاعدة جديدة من VertexElementNormal ، VertexEleتوينثيلا ertexColor ، VertexEleتوينتيلا غير طبيعي ، VertexEleتوينتيجنت أنغنت ، VertexEleتوينتيكا و erertexEليمنتس بيكنت. لا يؤثر It على الرمز الجانبي للمستخدم.
#### **تم تعديل ember ember إلى Aspose.ThreeD. nntities. class urbsCurve الفئة**
**تعريف ld ld**

{{< highlight "java" >}}

 System.Collections.Generic.List<double> KnotVectors{ get;}

{{< /highlight >}}

**تعريف ew**

{{< highlight "java" >}}

 IArrayList<double> KnotVectors{ get;}

{{< /highlight >}}
#### **تم تعديل ember ember إلى Aspose.ThreeD. nntities. NurbsDفئة irection**
**تعريف ld ld**

{{< highlight "java" >}}

 System.Collections.Generic.List<double> KnotVectors{ get;}

{{< /highlight >}}

**تعريف ew**

{{< highlight "java" >}}

 IArrayList<double> KnotVectors{ get;}

{{< /highlight >}}
