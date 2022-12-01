---
title: Aspose.3D for .NET 19,6 Utgivningsmeddelanden
type: docs
weight: 70
url: /sv/net/aspose-3d-for-net-19-6-release-notes/
---
{{% alert color="primary" %}} 

Denna sida innehåller utgåvans anteckningar för[Aspose.3D for .NET 19,6](https://www.nuget.org/packages/Aspose.3D/19.6.0)

{{% /alert %}} 
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|THREEDNET-511|Förbättra skapandet av cylinder|Ny funktion|
|THREEDNET-507|Förlora några material när du öppnar filen RVM|FelComment|
|THREEDNET-508|Systemet kan misslyckas med att tilldela deskriptor-inställning ibland i Vulkan renderare|FelComment|
### **Offentlig API och bakåts oförenliga förändringar**
Se förteckningen över eventuella ändringar i allmänheten API såsom lagts till, bytt namn, Avlägsnade eller förlåtna medlemmar samt eventuella icke-tillbaka-kompatibla förändringar till Aspose.3D for .NET. Om du har farhågor om någon förändring som anges, vänligen ta upp det om[Aspose.3D stödforum](https://forum.aspose.com/c/3d).
#### **Tillagd ny fastighet OffsetTop i klass Aspose.ThreeD.Enheter.Cylinder**
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
#### **Lagt ny fastighet OffsetBottom i klass Aspose.ThreeD.Enheter.Cylinder**
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

Provkod för att generera en cylinder med anpassad OffsetTop:

{{< highlight "java" >}}

 Scene scene = new Scene();

var fan = new Cylinder(2, 2, 10, 20, 1, false);

fan.OffsetTop = new Vector3(5, 3, 0);

scene.RootNode.CreateChildNode(fan).Transform.Translation = new Vector3(10, 0, 0);

var nonfan = new Cylinder(2, 2, 10, 20, 1, false);

scene.RootNode.CreateChildNode(nonfan);

scene.Save("test.obj", FileFormat.WavefrontOBJ);

{{< /highlight >}}

Förhandsgranskning:

![TOD:imageName_Av_Text:](aspose-3d-for-net-19-6-release-notes_1.png)

Den vänstra har.**OffsetTop**Inställd till (5, 3, 0), är det lätt att se att toplocket har flyttats och hela bålet påverkas också.
#### **Tillagd ny fastighet GenereraFanCylinder i klass Aspose.ThreeD.Enheter.Cylinder**
{{< highlight "java" >}}

 /// <summary>

/// Gets or sets whether to generate the fan-style cylinder when the ThetaLength is less than 2*PI, otherwise the model will not be cut.

/// </summary>

public bool GenerateFanCylinder

{

    get;set;

}

{{< /highlight >}}

Provkod för att generera en fläktcylinder och cylinder icke-fan-stil:

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

Förhandsgranskning:

![TOD:imageName_Av_Text:](aspose-3d-for-net-19-6-release-notes_2.png)

Den vänstra cylindern har GenerateFanCylinder = false och den högra har GenerateFanCylinder = true.
#### **Tillagd ny fastighet ShearTop i klass Aspose.ThreeD.Enheter.Cylinder**
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
#### **Tillagd ny fastighet ShearBottom i klass Aspose.ThreeD.Enheter.Cylinder**
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

Provkod för att visa användningen av ShearBottom(ShearTop):

{{< highlight "java" >}}

 Scene scene = new Scene();

var cylinder1 = new Cylinder(2, 2, 10, 20, 1, false);

cylinder1.ShearBottom = new Vector2(0, 0.83);// shear 47.5deg in xy plane(z-axis)

scene.RootNode.CreateChildNode(cylinder1).Transform.Translation = new Vector3(10, 0, 0);

var cylinder2 = new Cylinder(2, 2, 10, 20, 1, false);

scene.RootNode.CreateChildNode(cylinder2);

scene.Save("test.obj", FileFormat.WavefrontOBJ);

{{< /highlight >}}

Förhandsgranskning:

![TOD:imageName_Av_Text:](aspose-3d-for-net-19-6-release-notes_3.png)

Den vänstra cylindern har ShearBottom till (0, 0.83) medan den högra är en vanlig cylinder.
