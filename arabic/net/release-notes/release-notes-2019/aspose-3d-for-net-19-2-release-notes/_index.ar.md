---
title: Aspose.3D for .NET 19.2 tes elease ootes
type: docs
weight: 110
url: /ar/net/aspose-3d-for-net-19-2-release-notes/
---
{{% alert color="primary" %}} 

Tصفحته تحتوي على ملاحظات الإصدار ل[Aspose.3D for .NET 19.2](https://www.nuget.org/packages/Aspose.3D/19.2.0)

{{% /alert %}} 
## **Ements proو Cمعلقة**

|**Key**|**Sأوماري**|**Category**|
|:- |:- |:- |
|THREEDNET-472|قم بإنشاء هندسة ببثق الأشكال|New eature|
### **Public API و ackأكواردز hangمتوافق مع hangمعلقة**
See قائمة أي تغييرات أجريت على الجمهور API مثل إضافة أو إعادة تسميتها أو إزالتها أو إهمال الأعضاء وكذلك أي تغيير متوافق غير متخلف تم إجراؤه على Aspose.3D for .NET. If لديك مخاوف حول أي تغيير المدرجة ، يرجى رفع على[Aspose.3D دعم المنتدى](https://forum.aspose.com/c/3d).
#### **طريقة ded dded romromControPoinفي الفئة Aspose.ThreeD. nntities. Shape**
{{< highlight "java" >}}

 /// <summary>

/// Create a shape with specified control points with a default indices.

/// </summary>

/// <param name="controlPoints"></param>

/// <returns></returns>

public static Shape FromControlPoints(params Vector3[]controlPoints);

{{< /highlight >}}
#### **Added فئة جديدة Aspose.ThreeD. nntities. ininearExtrusion:**
{{< highlight "java" >}}

 /// <summary>

/// Linear extrusion takes a 2D shape as input and extends the shape in the 3rd dimension.

/// </summary>

public class LinearExtrusion : Entity, IMeshConvertible

{

    /// <summary>

    /// The base shape to be extruded.

    /// </summary>

    public Shape Shape {get; set;}

    /// <summary>

    /// The direction of extrusion, default value is (0, 0, 1) 

    /// </summary>

    public Vector3 Direction { get;set; }

    /// <summary>

    /// The height of the extruded geometry, default value is 1.0

    /// </summary>

    public double Height {get; set;}

    /// <summary>

    /// The slices of the twisted extruded geometry, default value is 1.

    /// </summary>

    public int Slices {get;set; }

    /// <summary>

    /// If this value is false, the linear extrusion Z range is from 0 to height, otherwise the range is from -height/2 to height/2.

    /// </summary>

    public bool Center { get;set; }

    /// <summary>

    /// The offset that used in twisting, default value is (0, 0, 0).

    /// </summary>

    public Vector3 TwistOffset { get; set; }

    /// <summary>

    /// The number of degrees of through which the shape is extruded.

    /// </summary>

    public double Twist { get; set; }

    /// <summary>

    /// Constructor of instance <see cref="LinearExtrusion"/>.

    /// </summary>

    public LinearExtrusion();

    /// <summary>

    /// Constructor of instance <see cref="LinearExtrusion"/>.

    /// </summary>

    public LinearExtrusion(Shape shape, double height);

}

{{< /highlight >}}
