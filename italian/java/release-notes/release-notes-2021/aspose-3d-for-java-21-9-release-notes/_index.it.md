---
title: Aspose.3D for Java Note di rilascio 21.9
type: docs
weight: 4
url: /it/java/aspose-3d-for-java-21-9-release-notes/
---
{{% alert color="primary" %}}

Questa pagina contiene le informazioni sulle note di rilascio per lo Aspose.3D for Java 21.9.

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


### Aggiunto nuovo metodo alla classe com.aspose.threed.PointCloud:

{{< highlight "java" >}}
    /**
     * Create a new point cloud instance from a geometry object.
     * Density is the number of points per unit triangle(Unit triangle are the triangle with maximum surface area from the mesh)
     * @param g Mesh or other geometry instance
     * @param density Number of points per unit triangle
     */
    public static PointCloud fromGeometry(Geometry g, int density);
{{< /highlight >}}


Il nuovo FromGeometry consente di specificare la densità dei punti distribuiti nei triangoli della geometria.

Codice del campione:

{{< highlight "java" >}}

        var prim = new Torus();
        var pc = PointCloud.fromGeometry(prim.toMesh(), 50);
        var s = new Scene(pc);
        s.save("point-cloud.glb", FileFormat.GLTF2_BINARY);

{{< /highlight >}}


### Aggiunti nuovi formati a class com.aspose.threed.FileFormat:

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


Codice del campione:

{{< highlight "java" >}}

        var prim = new Torus();
        var pc = PointCloud.fromGeometry(prim.toMesh(), 50);
        var s = new Scene(pc);
        s.save("point-cloud.glb", FileFormat.PCD);

{{< /highlight >}}