---
title: Lavorare con PointCloud
type: docs
weight: 110
url: /it/java/working-with-pointcloud/
description: Aspose.3D for Java consente di decodificare direttamente una mesh da un file Draco senza creare una scena utilizzando il metodo di decodifica della classe DracoFormat.
---
#  **Decodificare la maglia**
Aspose.3D for Java consente di decodificare direttamente una mesh da un file Draco senza creare una scena utilizzando il metodo [`decode`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat#decode-java.lang.String-) della classe [`DracoFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat). Il seguente frammento di codice mostra come utilizzare questa funzionalità:



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-pointcloud-DecodeMesh-1.java" >}}
#  **Code Mesh**
Aspose.3D for Java consente di codificare direttamente una mesh a sfera in un file Draco senza creare una scena utilizzando il metodo [`encode`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat#encode-com.aspose.threed.Entity-java.lang.String-) della classe [`DracoFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat). Il seguente frammento di codice mostra come utilizzare questa funzionalità:



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-pointcloud-EncodeMesh-1.java" >}}
#  **Codificare sfera come PointCloud**
Aspose.3D for Java consente di codificare una mesh sfera in file Draco come nuvola di punti utilizzando il metodo [`encode`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat#encode-com.aspose.threed.Entity-java.lang.String-com.aspose.threed.DracoSaveOptions-) della classe [`DracoFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat). Il seguente frammento di codice mostra come utilizzare questa funzionalità:



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-pointcloud-EncodeSphereAsPointCloud-1.java" >}}
#  **Codificare la maglia fino a PLY**
Aspose.3D for Java consente di codificare direttamente un file mesh in PLY senza creare una scena utilizzando il metodo [`encode`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat#encode-com.aspose.threed.Entity-java.lang.String-) della classe [`PlyFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat). Il seguente frammento di codice mostra come utilizzare questa funzionalità:



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-pointcloud-EncodeMeshToPly-1.java" >}}
#  **Decodificare mesh a partire da PLY**
Aspose.3D for Java consente di decodificare una nuvola mesh/point da un file PLY utilizzando il metodo [`decode`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat#decode-java.lang.String-) della classe [`PlyFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat). Il seguente frammento di codice mostra come utilizzare questa funzionalità:



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-pointcloud-EncodeMeshToPly-1.java" >}}
#  **Esporta a PLY come PointCloud**
Aspose.3D for Java consente di esportare una scena a PLY come PointCloud utilizzando il metodo [`encode`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat#encode-com.aspose.threed.Entity-java.lang.String-com.aspose.threed.PlySaveOptions-) della classe [`PlyFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat). Il seguente frammento di codice mostra come utilizzare questa funzionalità:



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-pointcloud-ExportToPlyAsPointCloud-1.java" >}}
#  **Esporta 3D scena come Point Cloud**
{{% alert color="primary" %}} 

Questa funzione è supportata dalla versione 19.8 o maggiore.

{{% /alert %}} 

Aspose.3D for Java consente di esportare una scena 3D come PointCloud utilizzando il metodo [`setPointCloud`](https://reference.aspose.com/3d/java/com.aspose.threed/ObjSaveOptions#setPointCloud-boolean-) della classe [`ObjSaveOptions`](https://reference.aspose.com/3d/java/com.aspose.threed/ObjSaveOptions). Il seguente frammento di codice mostra come utilizzare questa funzionalità:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-pointcloud-Export3DSceneAsPointCloud-1.java" >}}
