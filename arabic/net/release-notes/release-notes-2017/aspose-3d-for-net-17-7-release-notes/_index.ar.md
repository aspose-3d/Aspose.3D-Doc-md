---
title: Aspose.3D for .NET 17.7 tes elease ootes
type: docs
weight: 60
url: /ar/net/aspose-3d-for-net-17-7-release-notes/
---
{{% alert color="primary" %}} 

Tصفحته تحتوي على ملاحظات الإصدار ل[Aspose.3D for .NET 17.7](https://www.nuget.org/packages/Aspose.3D/17.7.0).

{{% /alert %}} 
## **Oأكثر ements المبروفات و hangمعلقة**

|**Key**|**Sأوماري**|**Category**|
|:- |:- |:- |
|THREEDNET-265|Add دعم تصدير المشهد 3D إلى تنسيق PLY.|ميزة ew ew|
|THREEDNET-271|Impيمس إنشاء مصفوفة التحويل.|ميزة ew ew|
|THREEDNET-270|Allow توليد شبكة من الصورة على نطاق رمادي كخريطة الارتفاع.|ميزة ew ew|
|THREEDNET-272|The FBX ملف ولدت لا يمكن تحريرها من قبل 3ds ماكس.|Bug|
|THREEDNET-274|يتم تلف UVs عند تصدير مشهد بتنسيق FBX.|Bug|
### **Public API و ackأكواردز hangمتوافق مع hangمعلقة**
See قائمة أي تغييرات أجريت على الجمهور API مثل إضافة أو إعادة تسميتها أو إزالتها أو إهمال الأعضاء وكذلك أي تغيير متوافق غير متخلف تم إجراؤه على Aspose.3D for .NET. If لديك مخاوف حول أي تغيير المدرجة ، يرجى رفع على[Aspose.3D دعم المنتدى](https://forum.aspose.com/c/3d/18).
#### **Adds emالجمر إلى Aspose.ThreeD.**
**C#**

{{< highlight "java" >}}

 /// <summary>

/// Creates a translation matrix 

/// </summary>

/// <param name="t"></param>

/// <returns></returns>

public static Matrix4 Translate(Vector3 t);

/// <summary>

/// Creates a translation matrix 

/// </summary>

/// <param name="tx"></param>

/// <param name="ty"></param>

/// <param name="tz"></param>

/// <returns></returns>

public static Matrix4 Translate(double tx, double ty, double tz);

/// <summary>

/// Create a scale matrix

/// </summary>

/// <param name="s"></param>

/// <returns></returns>

public static Matrix4 Scale(Vector3 s);

/// <summary>

/// Create a scale matrix

/// </summary>

/// <param name="s"></param>

/// <returns></returns>

public static Matrix4 Scale(double s);

/// <summary>

/// Create a scale matrix

/// </summary>

/// <param name="sx"></param>

/// <param name="sy"></param>

/// <param name="sz"></param>

/// <returns></returns>

public static Matrix4 Scale(double sx, double sy, double sz);

/// <summary>

/// Create a rotation matrix from euler angle

/// </summary>

/// <param name="eul">Rotation in radian</param>

/// <returns></returns>

public static Matrix4 RotateFromEuler(Vector3 eul);

/// <summary>

/// Create a rotation matrix from euler angle

/// </summary>

/// <param name="rx">Rotation in x axis in radian</param>

/// <param name="ry">Rotation in y axis in radian</param>

/// <param name="rz">Rotation in z axis in radian</param>

/// <returns></returns>

public static Matrix4 RotateFromEuler(double rx, double ry, double rz) 

/// <summary>

/// Create a rotation matrix by rotation angle and axis

/// </summary>

/// <param name="angle">Rotate angle in radian</param>

/// <param name="axis">Rotation axis</param>

/// <returns></returns>

public static Matrix4 Rotate(double angle, Vector3 axis);

/// <summary>

/// Create a rotation matrix from a quaternion

/// </summary>

/// <param name="rotate"></param>

/// <returns></returns>

public static Matrix4 Rotate(Quaternion rotate);



//Create a transform that translates (1, 0, 0) then rotates alone the y axis pi radian.

var m  = Matrix4.RotateFromEuler(0, Math.PI, 0) * Matrix4.Translate(1, 0, 0);

{{< /highlight >}}
#### **Classes dds فصول جديدة Aspose.ThreeD. tiliتيليتيز. ComposOrder و Aspose.ThreeD. tiliتيليتيز. ranransformBuilder**
Tانه تحويل باني يبسط إنشاء مصفوفة التحول من خلال سلسلة من العمليات.

**C#**

{{< highlight "java" >}}

 //use prepend order so the calculation is performed from left to right:

var m = (new TransformBuilder(ComposeOrder.Prepend))

    //Change the (x, y, z) into (x + 1, y, z)

    .Translate(1, 0, 0)

    //Rotate alone with the Y axis with 180deg will change the (x, y, z) into (-x, y, -z)

    .RotateEulerDegree(0, 180, 0)

    //Scale by 2 will change the (x, y, z) into (2x, 2y, 2z)

    .Scale(2)

    //change the (x, y, z) into (z, y, x)

    .Rearrange(Axis.ZAxis, Axis.YAxis, Axis.XAxis)

    .Matrix;



//Apply this matrix on a (0, 0, 0) vector, then we get the right result (0, 0, -2)

var t = m * Vector3.Origin;

{{< /highlight >}}
#### **Emالجمر تحديث إلى Aspose.ThreeD.**
Tتغيير له يقدم فئة جديدة Aspose.ThreeD. orormat. PlyFormat ، والذي يسمح لك لترميز شبكة واحدة بدلا من المشهد كله:

**C#**

{{< highlight "java" >}}

 public static readonly Aspose.ThreeD.FileFormat PLY;

//Changed to

public static readonly Aspose.ThreeD.Formats.PlyFormat PLY;



// sample code

// Create a cylinder object and save it to ply file

FileFormat.PLY.EncodeMesh(new Cylinder(), "cylinder.ply");

{{< /highlight >}}
#### **Adds فئة جديدة Aspose.ThreeD. ororالحصير.**
Ply تنسيق ليس لديه معيار رسمي ، قد يكون تطبيق مختلف تعريفات مختلفة من شكل فيرتكس ، هذه الفئة يسمح لك لتحديد تفاصيل تنسيق Ply.
Fأو مثال على اسم المكون الافتراضي لمكونات تنسيق الملمس هو "u' و" v' ، ولكن بعض التطبيقات تستخدم "و" t' ، ثم يمكنك تغيير الاسم باستخدام هذه الفئة:

**C#**

{{< highlight "java" >}}

 //Save as binary PLY format, the default value is ASCII

PlySaveOptions opt = new PlySaveOptions(FileContentType.Binary);

//change the components to 's' and 't'

opt.TextureCoordinateComponents.Item1 = "s";

opt.TextureCoordinateComponents.Item2 = "t";

//save the mesh

FileFormat.PLY.EncodeMesh(new Cylinder(), "cylinder.ply", opt);

{{< /highlight >}}
### **Uحكيم Examles**
Pالإيجار تحقق من قائمة المواضيع المساعدة المضافة أو updated في مستندات Aspose.3D Wiki:

1. [Convert esh esh من كائن واحد 3D في ملف PLY](/3d/ar/net/convert-mesh-of-a-single-3d-object-in-ply-file/)
1. [Impيمس إنشاء مصفوفة التحول من قبل عمليات السلسلة](/3d/ar/net/simplify-the-creation-of-transformation-matrix-by-the-chain-operations/)
