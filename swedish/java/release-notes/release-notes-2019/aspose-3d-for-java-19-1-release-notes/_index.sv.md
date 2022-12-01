---
title: Aspose.3D for Java 19,1 Utgivning
type: docs
weight: 120
url: /sv/java/aspose-3d-for-java-19-1-release-notes/
---
{{% alert color="primary" %}} 

Denna sida innehåller utgivningsanmärkningar för Aspose.3D for Java 19.1.

{{% /alert %}} 
## **Förbättringar och förändringar**

|**Sammanfattning**|**Kategori**|
|:- |:- |
|UV-atlasalgoritm|Ny funktion|
|AMF Exportör|Ny funktion|
|Arkivbaserat filformat|Ny funktion|

## **Offentlig API och bakåts oförenliga förändringar**
Se förteckningen över eventuella ändringar i allmänheten API såsom lagts till, bytt namn, Avlägsnade eller förlåtna medlemmar samt eventuella icke-tillbaka-kompatibla förändringar till Aspose.3D for Java. Om du har farhågor om någon förändring som anges, vänligen ta upp det om[Aspose.3D stödforum](https://forum.aspose.com/c/3d).

**Tillagd klass com.pose.3reed.AMFSaveOptions:**

{{< highlight "java" >}}

 /**

 * Save options for AMF

 */

public class AMFSaveOptions extends SaveOptions

{ 



    /**

     * Whether to use compression to reduce the final file size, default value is true

     */

    public boolean getEnableCompression();



    /**

     * Whether to use compression to reduce the final file size, default value is true

     * @param value New value

     */

    public void setEnableCompression(boolean value);

}

{{< /highlight >}}

**Ny medlem lagt till i klassen 'com.aspose. Threed.PolygonModifier':**

{{< highlight "java" >}}

     /**

     * Generate UV data from the given input mesh and specified normal data.

     * @param mesh The input mesh

     * @param normals The normal data

     * @return Generated UV data

     */

    public static VertexElementUV generateUV(Mesh mesh, VertexElementNormal normals);

    /**

     * Generate UV data from the given input mesh

     * @param mesh The input mesh

     * @return Generated UV data

     */

    public static VertexElementUV generateUV(Mesh mesh);

{{< /highlight >}}




