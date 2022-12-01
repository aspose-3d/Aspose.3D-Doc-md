---
title: Aspose.3D for .NET 19,2 Utgivning
type: docs
weight: 110
url: /sv/net/aspose-3d-for-net-19-2-release-notes/
---
{{% alert color="primary" %}} 

Denna sida innehåller utgåvans anteckningar för[Aspose.3D for .NET 19,2](https://www.nuget.org/packages/Aspose.3D/19.2.0)

{{% /alert %}} 
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|THREEDNET-472|Skapa geometri genom att extrudera former|Ny funktion|
### **Offentlig API och bakåts oförenliga förändringar**
Se förteckningen över eventuella ändringar i allmänheten API såsom lagts till, bytt namn, Avlägsnade eller förlåtna medlemmar samt eventuella icke-tillbaka-kompatibla förändringar till Aspose.3D for .NET. Om du har farhågor om någon förändring som anges, vänligen ta upp det om[Aspose.3D stödforum](https://forum.aspose.com/c/3d).
#### **Tillagd metod FrånControlPoints i klass Aspose.ThreeD.Enheter.Shape**
{{< highlight "java" >}}

 /// <summary>

/// Create a shape with specified control points with a default indices.

/// </summary>

/// <param name="controlPoints"></param>

/// <returns></returns>

public static Shape FromControlPoints(params Vector3[]controlPoints);

{{< /highlight >}}
#### **Tillagd ny klass Aspose.ThreeD Enheter.LinearExtrusion:**
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
