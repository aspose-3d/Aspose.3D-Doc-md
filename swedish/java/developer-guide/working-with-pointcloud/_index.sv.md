---
title: Arbeta med PointCloudName
type: docs
weight: 110
url: /sv/java/working-with-pointcloud/
description: Aspose. 3D for Java tillåter avkodning av ett mesh från en Draco-fil direkt utan att bygga en scen med hjälp av filen avkodningsmetod för DracoFormat-klassen.
---
#  **Avkoda mask**
Aspose. 3D for Java tillåter avkodning av ett mesh från en Draco-fil direkt utan att bygga en scen med hjälp av filen [`decode`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat#decode-java.lang.String-) metod för [`DracoFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat) klass. Följande kodsnutt visar hur denna funktionalitet ska användas:



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-pointcloud-DecodeMesh-1.java" >}}
#  **Koda mesh**
Aspose. 3D for Java tillåter kodning av ett sfärsnät till en Draco-fil direkt utan att bygga en scen med användning av en scen. [`encode`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat#encode-com.aspose.threed.Entity-java.lang.String-)-metoden i [`DracoFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat) klassen. Följande kodsnutt visar hur denna funktionalitet ska användas:



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-pointcloud-EncodeMesh-1.java" >}}
#  **Koda sfären som PointCloudName**
Aspose. 3D for Java tillåter kodning av ett sfärsnät till filen Draco som ett punktmoln med [`encode`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat#encode-com.aspose.threed.Entity-java.lang.String-com.aspose.threed.DracoSaveOptions-) metod för [`DracoFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat) klass. Följande kodsnutt visar hur denna funktionalitet ska användas:



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-pointcloud-EncodeSphereAsPointCloud-1.java" >}}
#  **Koda mesh till PLY.**
Aspose.3D for Java allows encoding a mesh to PLY file directly without building a scene using the [`encode`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat#encode-com.aspose.threed.Entity-java.lang.String-) method of [`PlyFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat) class. The following code snippet shows how to use this functionality:



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-pointcloud-EncodeMeshToPly-1.java" >}}
#  **Avkoda mesh från PLY.**
Aspose. 3D for Java gör det möjligt att avkoda ett mesh/punkt moln från en PLY-fil med [`decode`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat#decode-java.lang.String-)-metoden. för [`PlyFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat) klass. Följande kodsnutt visar hur denna funktionalitet ska användas:



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-pointcloud-EncodeMeshToPly-1.java" >}}
#  **Exportera till PLY som PointCloud?**
Aspose. 3D for Java gör det möjligt att exportera en scen till PLY som PointCloud med [`encode`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat#encode-com.aspose.threed.Entity-java.lang.String-com.aspose.threed.PlySaveOptions-)-metoden för [`PlyFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat) klassen. .. Följande kodsnutt visar hur denna funktionalitet ska användas:



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-pointcloud-ExportToPlyAsPointCloud-1.java" >}}
#  **Exportera 3D Scene som punktmoln**
{{% alert color="primary" %}} 

Denna funktion stöds av version 19.8 eller större.

{{% /alert %}} 

Aspose. 3D for Java tillåter export av en 3D scen som PointCloud med [`setPointCloud`](https://reference.aspose.com/3d/java/com.aspose.threed/ObjSaveOptions#setPointCloud-boolean-)-metoden för [`ObjSaveOptions`](https://reference.aspose.com/3d/java/com.aspose.threed/ObjSaveOptions) klass. Följande kodsnutt visar hur denna funktionalitet ska användas:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-pointcloud-Export3DSceneAsPointCloud-1.java" >}}
