---
title: Aspose.3D for .NET 21,9 Utgivning
type: docs
weight: 4
url: /sv/net/aspose-3d-for-net-21-9-release-notes/
---
{{% alert color="primary" %}}

Denna sida innehåller release anteckningar för Aspose.3D for .NET 21.9.

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


### Lagt till ny metod till klass Aspose.ThreeD.Enheter.PointCloud:

{{< highlight "csharp" >}}
        /// <summary>
        /// Create a new point cloud instance from a geometry object.
        /// Density is the number of points per unit triangle(Unit triangle are the triangle with maximum surface area from the mesh)
        /// </summary>
        /// <param name="g">Mesh or other geometry instance</param>
        /// <param name="density">Number of points per unit triangle</param>
        /// <returns></returns>
        public static Aspose.ThreeD.Entities.PointCloud FromGeometry(Aspose.ThreeD.Entities.Geometry g, int density);
{{< /highlight >}}


Den nya FromGeometry låter dig ange densiteten av distribuerade punkter i geometrins trianglar.

Provkod:

{{< highlight "csharp" >}}

        var prim = new Torus();
        var pc = PointCloud.FromGeometry(prim.ToMesh(), 50);
        var s = new Scene(pc);
        s.Save("point-cloud.glb", FileFormat.GLTF2_Binary);

{{< /highlight >}}


### Lagt till nya format i klass Aspose.ThreeD.FileFormat:

{{< highlight "csharp" >}}
        public static readonly Aspose.ThreeD.FileFormat Xyz;
        public static readonly Aspose.ThreeD.FileFormat Pcd;
        public static readonly Aspose.ThreeD.FileFormat PcdBinary;
{{< /highlight >}}


Provkod:

{{< highlight "csharp" >}}

        var prim = new Torus();
        var pc = PointCloud.FromGeometry(prim.ToMesh(), 50);
        var s = new Scene(pc);
        s.Save("point-cloud.glb", FileFormat.Pcd);

{{< /highlight >}}