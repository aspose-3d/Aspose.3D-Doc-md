---
title: Aspose.3D for Java 19,6 Utgivningsmeddelanden
type: docs
weight: 70
url: /sv/java/aspose-3d-for-java-19-6-release-notes/
---
{{% alert color="primary" %}} 

Denna sida innehåller utgåvans anteckningar för[Aspose.3D for Java 19,6](https://releases.aspose.com/java/repo/com/aspose/aspose-3d//19.6)

{{% /alert %}} 
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|THREEDNET-511|Förbättra skapandet av cylinder|Ny funktion|
|THREEDNET-507|Förlora några material när du öppnar filen RVM|FelComment|
|THREEDNET-508|Systemet kan misslyckas med att tilldela deskriptor-inställning ibland i Vulkan renderare|FelComment|
### **Offentlig API och bakåts oförenliga förändringar**
Se förteckningen över eventuella ändringar i allmänheten API såsom lagts till, bytt namn, Avlägsnade eller förlåtna medlemmar samt eventuella icke-tillbaka-kompatibla förändringar till Aspose.3D for Java. Om du har farhågor om någon förändring som anges, vänligen ta upp det om[Aspose.3D stödforum](https://forum.aspose.com/c/3d).
#### **Tillagd ny fastighet OffsetTop i klass com.aspose.tre.Cylinder**
{{< highlight "java" >}}

 /**

 * Gets the vertices transformation offset of the top side.

 */

public Vector3 getOffsetTop();

/**

 * Sets the vertices transformation offset of the top side.

 * @param value New value

 */

public void setOffsetTop(Vector3 value);

{{< /highlight >}}
#### **Lagt ny fastighet OffsetBorrom i klass com.aspose.tre.Cylinder**
{{< highlight "java" >}}

 /**

 * Gets the vertices transformation offset of the bottom side.

 */

public Vector3 getOffsetBottom();

/**

 * Sets the vertices transformation offset of the bottom side.

 * @param value New value

 */

public void setOffsetBottom(Vector3 value);

{{< /highlight >}}

Provkod för att generera en cylinder med anpassad OffsetTop:

{{< highlight "java" >}}

 Scene scene = new Scene();

Cylinder cylinder1 = new Cylinder(2, 2, 10, 20, 1, false);

cylinder1.setOffsetTop(new Vector3(5, 3, 0));

scene.getRootNode().createChildNode(cylinder1).getTransform().setTranslation(10, 0, 0);

Cylinder cylinder2 = new Cylinder(2, 2, 10, 20, 1, false);

scene.getRootNode().createChildNode(cylinder2);

scene.save("test.obj", FileFormat.WAVEFRONTOBJ);

{{< /highlight >}}

Förhandsgranskning:

![TOD:imageName_Av_Text:](aspose-3d-for-java-19-6-release-notes_1.png)

Den vänstra har.**OffsetTop**Inställd till (5, 3, 0), är det lätt att se att toplocket har flyttats och hela bålet påverkas också.
#### **Tillagd ny egenskap GenereraFanCylinder i klass com.aspose. Threed.Cylinder**
{{< highlight "java" >}}

 /**

 * Gets whether to generate the fan-style cylinder when the ThetaLength is less than 2*PI, otherwise the model will not be cut.

 */

public boolean getGenerateFanCylinder();

/**

 * Sets whether to generate the fan-style cylinder when the ThetaLength is less than 2*PI, otherwise the model will not be cut.

 * @param value New value

 */

public void setGenerateFanCylinder(boolean value);

{{< /highlight >}}

Provkod för att generera en fläktcylinder och cylinder icke-fan-stil:

{{< highlight "java" >}}

 Scene scene = new Scene();

Cylinder fan = new Cylinder(2, 2, 10, 20, 1, false);

fan.setGenerateFanCylinder(true);

fan.setThetaLength(MathUtils.toRadian(270.0));

scene.getRootNode().createChildNode(fan).getTransform().setTranslation(10, 0, 0);

Cylinder nonfan = new Cylinder(2, 2, 10, 20, 1, false);

scene.getRootNode().createChildNode(nonfan);

scene.save("test.obj", FileFormat.WAVEFRONTOBJ);

{{< /highlight >}}

Förhandsgranskning:

![TOD:imageName_Av_Text:](aspose-3d-for-java-19-6-release-notes_2.png)

Den vänstra cylindern har GenerateFanCylinder = false och den högra har GenerateFanCylinder = true.
#### **Tillagd ny fastighet ShearTop i klass com.aspose.tre.Cylinder**
{{< highlight "java" >}}

 **

 * Gets of the shear transform of the top side, vector stores the (x-axis, z-axis) shear value that measured in radian, default value is (0, 0)

 */

public Vector2 getShearTop();

/**

 * Sets of the shear transform of the top side, vector stores the (x-axis, z-axis) shear value that measured in radian, default value is (0, 0)

 * @param value New value

 */

public void setShearTop(Vector2 value)

{{< /highlight >}}
#### **Tillagd ny fastighet ShearBottom i klass com.aspose.tre.Cylinder.**
{{< highlight "java" >}}

 /**

 * Gets of the shear transform of the bottom side, vector stores the (x-axis, z-axis) shear value that measured in radian, default value is (0, 0)

 */

public Vector2 getShearBottom();

/**

 * Sets of the shear transform of the bottom side, vector stores the (x-axis, z-axis) shear value that measured in radian, default value is (0, 0)

 * @param value New value

 */

public void setShearBottom(Vector2 value);

{{< /highlight >}}

Provkod för att visa användningen av ShearBottom(ShearTop):

{{< highlight "java" >}}

 Scene scene = new Scene();

Cylinder cylinder1 = new Cylinder(2, 2, 10, 20, 1, false);

cylinder1.setShearBottom(new Vector2(0, 0.83));//shear 47.5deg in xy plane(z-axis)

scene.getRootNode().createChildNode(cylinder1).getTransform().setTranslation(10, 0, 0);

Cylinder cylinder2 = new Cylinder(2, 2, 10, 20, 1, false);

scene.getRootNode().createChildNode(cylinder2);

scene.save("test.obj", FileFormat.WAVEFRONTOBJ);

{{< /highlight >}}

Förhandsgranskning:

![TOD:imageName_Av_Text:](aspose-3d-for-java-19-6-release-notes_3.png)

Den vänstra cylindern har ShearBottom till (0, 0.83) medan den högra är en vanlig cylinder.
