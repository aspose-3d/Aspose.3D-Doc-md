---
title: Arbeta med PointCloudName
type: docs
weight: 110
url: /sv/java/working-with-pointcloud/
description: Aspose.3D for Java gör det möjligt att avkoda en mesh från en Draco-fil direkt utan att bygga en scen som använder avkodningsmetoden i DracoFormat klassen.
---
# **Avkoda mask**
Aspose.3D for Java gör det möjligt att avkoda en mesh från en Draco-fil direkt utan att bygga en scen som använder [`decode`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat#decode-java.lang.String-) metod [`DracoFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat) klass. Följande kodsnutt visar hur denna funktionalitet ska användas:



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-pointcloud-DecodeMesh-1.java" >}}
# **Koda mesh**
Aspose.3D for Java tillåter kodning av en sfärmask till en fil Draco direkt utan byggnad en scen som använder [`encode`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat#encode-com.aspose.threed.Entity-java.lang.String-) metoden [`DracoFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat) klass. Följande kodsnutt visar hur denna funktionalitet ska användas:



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-pointcloud-EncodeMesh-1.java" >}}
# **Koda sfären som PointCloudName**
Aspose.3D for Java tillåter kodning av en sfärsmask till Draco fil som ett punktmoln . med [`encode`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat#encode-com.aspose.threed.Entity-java.lang.String-com.aspose.threed.DracoSaveOptions-)-metoden [`DracoFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat). Följande kodsnutt visar hur denna funktionalitet ska användas:



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-pointcloud-EncodeSphereAsPointCloud-1.java" >}}
# **Koda mesh till PLY**
Aspose.3D for Java gör det möjligt att koda en mesh till PLY fil direkt utan att bygga en scen. med [`encode`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat#encode-com.aspose.threed.Entity-java.lang.String-)-metoden [`PlyFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat)-klass. Följande kodsnutt visar hur denna funktionalitet ska användas:



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-pointcloud-EncodeMeshToPly-1.java" >}}
# **Avkoda mask från PLY**
Aspose.3D for Java tillåter avkodning av ett nät/punktsmoln från en PLY-fil med hjälp av PLY [`decode`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat#decode-java.lang.String-)-metoden för klass [`PlyFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat). Följande kodsnutt visar hur denna funktionalitet ska användas:



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-pointcloud-EncodeMeshToPly-1.java" >}}
# **Exportera till PLY som PointCloud.**
Aspose.3D for Java tillåter att exportera en scen till PLY som PointCloud med hjälp av 076133488 1 metod [`PlyFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat) klass. Följande kodsnutt visar hur denna funktionalitet ska användas:



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-pointcloud-ExportToPlyAsPointCloud-1.java" >}}
# **Export 3D scen som Point Cloud**
{{% alert color="primary" %}} 

Denna funktion stöds av version 19.8 eller större.

{{% /alert %}} 

Aspose.3D for Java gör det möjligt att exportera en 3D scen som PointCloud med hjälp av [`setPointCloud`](https://reference.aspose.com/3d/java/com.aspose.threed/ObjSaveOptions#setPointCloud-boolean-) metoden [`ObjSaveOptions`](https://reference.aspose.com/3d/java/com.aspose.threed/ObjSaveOptions) klass. Följande kodsnutt visar hur denna funktionalitet ska användas:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-pointcloud-Export3DSceneAsPointCloud-1.java" >}}
