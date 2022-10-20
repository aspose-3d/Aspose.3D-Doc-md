---
title: Aspose.3D for Java 19,5 Utgivning
type: docs
weight: 80
url: /sv/java/aspose-3d-for-java-19-5-release-notes/
---
{{% alert color="primary" %}} 

Denna sida innehåller utgåvans anteckningar för[Aspose.3D for Java 19,5](https://releases.aspose.com/java/repo/com/aspose/aspose-3d//19.5)

{{% /alert %}} 
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|THREEDNET-501|Integrera med senaste Dynabic.Meterad|Förbättring|
|THREEDNET-505|Tillåt ändra planets orientering genom att ange ett upp normalt|Förbättring|
|THREEDNET-489|Shadow fungerar inte i Vulkan renderaren|FelComment|
|THREEDNET-504|Draco skapad från STL filen är trasig|FelComment|

## **Offentlig API och bakåts oförenliga förändringar**
Se förteckningen över eventuella ändringar i allmänheten API såsom lagts till, bytt namn, Avlägsnade eller förlåtna medlemmar samt eventuella icke-tillbaka-kompatibla förändringar till Aspose.3D for Java. Om du har farhågor om någon förändring som anges, vänligen ta upp det om[Aspose.3D stödforum](https://forum.aspose.com/c/3d).

**Lagt till ny fastighet * Radius* i klass com.aspose.tre.Plane**

{{< highlight "java" >}}

 /**

 * Gets the up vector of the plane, default value is (0, 1, 0), this affects the generation of the plane

 */

public Vector3 getUp();

/**

 * Sets the up vector of the plane, default value is (0, 1, 0), this affects the generation of the plane

 * @param value New value

 */

public void setUp(Vector3 value);

{{< /highlight >}}

Kod för att ange radie per egenskap istället för konstruktorargument:

{{< highlight "java" >}}

 Scene scene = new Scene();

Plane plane = new Plane();

plane.setUp(new Vector3(1, 1, 3));

scene.getRootNode().createChildNode(plane);

//This will generate a plane that has customized orientation

scene.save("test.obj", FileFormat.WAVEFRONTOBJ);

{{< /highlight >}}

**Lagt till ny metod "getConsumptionCredit" i klass com.aspose.3reed.Metered**

{{< highlight "java" >}}

 /**

\* Gets consumption credit

\* @return consumption quantity

*/

public static double getConsumptionCredit() throws Exception;

{{< /highlight >}}

Får konsumtionskredit för innevarande månad, som används av Dynabic.Meterad faktureringstjänst.
