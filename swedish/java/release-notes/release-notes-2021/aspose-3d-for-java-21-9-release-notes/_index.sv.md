---
title: Aspose.3D for Java 21,9 Utgivning
type: docs
weight: 4
url: /sv/java/aspose-3d-for-java-21-9-release-notes/
---
{{% alert color="primary" %}}

Denna sida innehåller release anteckningar för Aspose.3D for Java 21.9.

{{% /alert %}}
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|THREEDNET-930 |Lägg till PCD- exportstöd|Ny funktion|
|THREEDNET-926 |Lägg till stöd för import av XYZ|Ny funktion|
|THREEDNET-927 |Lägg till stöd för export av XYZ|Ny funktion|
|THREEDNET-938 |Algoritm för generation av punktmoln på triangelområdet.|Ny funktion|
|THREEDNET-932 |Lägg till stöd för punkt molnimport i format A3DW|Ny funktion|
|THREEDNET-931 |Lägg till Point Cloud export stöd i A3DW|Funktion|
|THREEDNET-946 |Fast PointCloud kan inte exporteras till PLY-format.|Felrättning|
|THREEDNET-934 |Omvandling från USDZ till OBJ resulterar i undantag|Felrättning|
|THREEDNET-936 |Lås påstående orsakad av GC FBX importör|Förbättring|


## API ändringar ##


De flesta förändringar i 21,9 är PointCloud relaterade, lagt XYZ/PCD stöd för PointCloud, Export av fast punkt moln i PLY. tillagd PointCloud import / export / överföring stöd A3DW/HTML.


### Lagt till ny metod till klass com.aspose.treed.PointCloud:

{{< highlight "java" >}}
    /**
     * Create a new point cloud instance from a geometry object.
     * Density is the number of points per unit triangle(Unit triangle are the triangle with maximum surface area from the mesh)
     * @param g Mesh or other geometry instance
     * @param density Number of points per unit triangle
     */
    public static PointCloud fromGeometry(Geometry g, int density);
{{< /highlight >}}


Den nya FromGeometry låter dig ange densiteten av distribuerade punkter i geometrins trianglar.

Provkod:

{{< highlight "java" >}}

        var prim = new Torus();
        var pc = PointCloud.fromGeometry(prim.toMesh(), 50);
        var s = new Scene(pc);
        s.save("point-cloud.glb", FileFormat.GLTF2_BINARY);

{{< /highlight >}}


### Lagt till nya format till klass com.aspose.treed.FileFormat:

{{< highlight "java" >}}
    /**
     * Xyz point cloud file
     */
    public static final FileFormat XYZ;
    /**
     * PCL Point Cloud Data file in ASCII mode
     */
    public static final FileFormat PCD;
    /**
     * PCL Point Cloud Data file in Binary mode
     */
    public static final FileFormat PCD_BINARY;

{{< /highlight >}}


Provkod:

{{< highlight "java" >}}

        var prim = new Torus();
        var pc = PointCloud.fromGeometry(prim.toMesh(), 50);
        var s = new Scene(pc);
        s.save("point-cloud.glb", FileFormat.PCD);

{{< /highlight >}}