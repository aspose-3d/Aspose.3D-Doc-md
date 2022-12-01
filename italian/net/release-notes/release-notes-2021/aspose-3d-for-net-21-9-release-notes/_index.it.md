---
title: Aspose.3D for .NET Note di rilascio 21.9
type: docs
weight: 4
url: /it/net/aspose-3d-for-net-21-9-release-notes/
---
{{% alert color="primary" %}}

Questa pagina contiene le informazioni sulle note di rilascio per lo Aspose.3D for .NET 21.9.

{{% /alert %}}
## **Miglioramenti e modifiche**

|**Chiave**|**Riassunto**|**Categoria**|
|:- |:- |:- |
|THREEDNET-930 |Aggiungi supporto per l'esportazione PCD|Nuova funzione|
|THREEDNET-926 |Aggiungi supporto all'importazione XYZ|Nuova funzione|
|THREEDNET-927 |Aggiungi supporto per l'esportazione XYZ|Nuova funzione|
|THREEDNET-938 |Algoritmo di generazione della superficie della nuvola di punti basato sull'area del triangolo.|Nuova funzione|
|THREEDNET-932 |Aggiungi supporto per l'importazione di Point Cloud in formato A3DW|Nuova funzione|
|THREEDNET-931 |Aggiungi supporto per l'esportazione di Point Cloud in formato A3DW|Caratteristica|
|THREEDNET-946 |PointCloud fisso non può essere esportato in formato PLY|Correzione di bug|
|THREEDNET-934 |La conversione da USDZ a OBJ risulta in eccezione|Correzione di bug|
|THREEDNET-936 |Lotta contro il blocco causata da GC nell'importatore FBX|Miglioramento|


## API modifiche ##


La maggior parte delle modifiche in 21.9 sono relative a PointCloud, aggiunto il supporto XYZ/PCD per PointCloud, l'esportazione di fixed Point Cloud in PLY, aggiunto il supporto di importazione/esportazione/rendering di PointCloud in A3DW/HTML.


### Aggiunto nuovo metodo alla classe Aspose.ThreeD.Entities.PointCloud:

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


Il nuovo FromGeometry consente di specificare la densità dei punti distribuiti nei triangoli della geometria.

Codice del campione:

{{< highlight "csharp" >}}

        var prim = new Torus();
        var pc = PointCloud.FromGeometry(prim.ToMesh(), 50);
        var s = new Scene(pc);
        s.Save("point-cloud.glb", FileFormat.GLTF2_Binary);

{{< /highlight >}}


### Aggiunti nuovi formati alla classe Aspose.ThreeD.FileFormat:

{{< highlight "csharp" >}}
        public static readonly Aspose.ThreeD.FileFormat Xyz;
        public static readonly Aspose.ThreeD.FileFormat Pcd;
        public static readonly Aspose.ThreeD.FileFormat PcdBinary;
{{< /highlight >}}


Codice del campione:

{{< highlight "csharp" >}}

        var prim = new Torus();
        var pc = PointCloud.FromGeometry(prim.ToMesh(), 50);
        var s = new Scene(pc);
        s.Save("point-cloud.glb", FileFormat.Pcd);

{{< /highlight >}}