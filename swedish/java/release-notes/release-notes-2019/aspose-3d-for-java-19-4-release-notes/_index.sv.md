---
title: Aspose.3D for Java 19,4 Utgivning
type: docs
weight: 90
url: /sv/java/aspose-3d-for-java-19-4-release-notes/
---
{{% alert color="primary" %}} 

Denna sida innehåller utgåvans anteckningar för[Aspose.3D for Java 19,4](https://releases.aspose.com/java/repo/com/aspose/aspose-3d//19.4)

{{% /alert %}} 
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|THREEDNET-483 |Stöd för format VRML|Ny funktion|
|THREEDJAVA-26|Utgivningsstöd för Aspose.3D for Java|Ny funktion|
|THREEDNET-496 |FBX7500Binarisexportfrågor|FelComment|

## **Offentlig API och bakåts oförenliga förändringar**

Se förteckningen över eventuella ändringar i allmänheten API såsom lagts till, bytt namn, Avlägsnade eller förlåtna medlemmar samt eventuella icke-tillbaka-kompatibla förändringar till Aspose.3D for Java. Om du har farhågor om någon förändring som anges, vänligen ta upp det om[Aspose.3D stödforum](https://forum.aspose.com/c/3d).

**Lagt ny fastighet Radius i klass com.aspose.tre.Sphere.**

{{< highlight "java" >}}

 /**

 * Gets the radius of the sphere.

 */

public double getRadius();

/**

 * Sets the radius of the sphere.

 * @param value New value

 */

public void setRadius(double value);

{{< /highlight >}}

Kod för att ange radie per egenskap istället för konstruktorargument:

{{< highlight "java" >}}

 Scene scene = new Scene();

Sphere sphere = new Sphere();

sphere.setRadius(10);

scene.getRootNode().createChildNode(sphere);

scene.save("sphere.obj", FileFormat.WAVEFRONTOBJ);

{{< /highlight >}}

**Lagt till nytt filformat VRML i klass com. Förmodligen. Tre. Filformat och com. Förmodligen. Tre. FilformattypName**

{{< highlight "java" >}}

 /**

 * The Virtual Reality Modeling Language

 */

public static final FileFormat VRML;

{{< /highlight >}}

Aspose.3D kan automatiskt detektera VRML format, så FileFormat oftast ignoreras i metoden Open. Provkod:

{{< highlight "java" >}}

 Scene scene = new Scene();

scene.open("test.wrl");

{{< /highlight >}}
