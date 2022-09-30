---
title: Aspose.3D for Java 19,2 Utgivning
type: docs
weight: 110
url: /sv/java/aspose-3d-for-java-19-2-release-notes/
---
{{% alert color="primary" %}} 

Denna sida innehåller publiceringsanmärkningar för Aspose.3D for Java 19.2

{{% /alert %}} 
## **Förbättringar och förändringar**

|**Sammanfattning**|**Kategori**|
|:- |:- |
|Skapa geometri genom att extrudera former|Ny funktion|

## **Offentlig API och bakåts oförenliga förändringar**
Se förteckningen över eventuella ändringar i allmänheten API såsom lagts till, bytt namn, Avlägsnade eller förlåtna medlemmar samt eventuella icke-tillbaka-kompatibla förändringar till Aspose.3D for Java. Om du har farhågor om någon förändring som anges, vänligen ta upp det om[Aspose.3D stödforum](https://forum.aspose.com/c/3d).

**Lagt till metod FrånControlPoints i klassen 'com.aspose.treed.Shape':**

{{< highlight "java" >}}

     /**

     * Create a shape with specified control points with a default indices.

     * @param controlPoints 

     */

    public static Shape fromControlPoints(Vector3... controlPoints);

{{< /highlight >}}

**Lagt till ny klass 'com.aspose. Threed.LinearExtrusion':**

{{< highlight "java" >}}

 /**

 * Linear extrusion takes a 2D shape as input and extends the shape in the 3rd dimension.

 */

public class LinearExtrusion extends Entity implements IMeshConvertible

{

    /**

     * The base shape to be extruded.

     */

    public Shape getShape();



    /**

     * The base shape to be extruded.

     * @param value New value

     */

    public void setShape(Shape value);



    /**

     * The direction of extrusion, default value is (0, 0, 1)

     */

    public Vector3 getDirection();



    /**

     * The direction of extrusion, default value is (0, 0, 1)

     * @param value New value

     */

    public void setDirection(Vector3 value);



    /**

     * The height of the extruded geometry, default value is 1.0

     */

    public double getHeight();



    /**

     * The height of the extruded geometry, default value is 1.0

     * @param value New value

     */

    public void setHeight(double value);



    /**

     * The slices of the twisted extruded geometry, default value is 1.

     */

    public int getSlices();



    /**

     * The slices of the twisted extruded geometry, default value is 1.

     * @param value New value

     */

    public void setSlices(int value);



    /**

     * If this value is false, the linear extrusion Z range is from 0 to height, otherwise the range is from -height/2 to height/2.

     */

    public boolean getCenter();



    /**

     * If this value is false, the linear extrusion Z range is from 0 to height, otherwise the range is from -height/2 to height/2.

     * @param value New value

     */

    public void setCenter(boolean value);



    /**

     * The offset that used in twisting, default value is (0, 0, 0).

     */

    public Vector3 getTwistOffset();



    /**

     * The offset that used in twisting, default value is (0, 0, 0).

     * @param value New value

     */

    public void setTwistOffset(Vector3 value);



    /**

     * The number of degrees of through which the shape is extruded.

     */

    public double getTwist();



    /**

     * The number of degrees of through which the shape is extruded.

     * @param value New value

     */

    public void setTwist(double value);



    /**

     * Constructor of instance {@link com.aspose.threed.LinearExtrusion}.

     */

    public LinearExtrusion();



    /**

     * Constructor of instance {@link com.aspose.threed.LinearExtrusion}.

     */

    public LinearExtrusion(Shape shape, double height);



    /**

     * Convert the extrusion to mesh.

     */

    public Mesh toMesh();

}

{{< /highlight >}}




