---
title: Mit Point Cloud arbeiten
type: docs
weight: 110
url: /de/java/working-with-pointcloud/
description: Aspose.3D for Java ermöglicht das direkte Decodieren eines Netzes aus einer Draco-Datei, ohne eine Szene mit der Dekodierung methode der DracoFormat-Klasse zu erstellen.
---
#  **Netz entschlüsseln**
Aspose.3D for Java ermöglicht das direkte Decodieren eines Netzes aus einer Draco-Datei, ohne eine Szene mit der [`decode`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat#decode-java.lang.String-)-Methode der [`DracoFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat)-Klasse zu erstellen. Das folgende Code-Snippet zeigt, wie diese Funktional ität verwendet wird:



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-pointcloud-DecodeMesh-1.java" >}}
#  **Maschen kodieren**
Aspose.3D for Java ermöglicht die direkte Codierung eines Kugel netzes in eine Draco-Datei, ohne eine Szene mit der [`encode`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat#encode-com.aspose.threed.Entity-java.lang.String-)-Methode der [`DracoFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat)-Klasse zu erstellen. Das folgende Code-Snippet zeigt, wie diese Funktional ität verwendet wird:



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-pointcloud-EncodeMesh-1.java" >}}
#  **Kugel als Point Cloud codieren**
Aspose.3D for Java ermöglicht das Codieren eines Kugel netzes in Draco-Datei als Punktwolke mit der [`encode`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat#encode-com.aspose.threed.Entity-java.lang.String-com.aspose.threed.DracoSaveOptions-)-Methode der [`DracoFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat)-Klasse. Das folgende Code-Snippet zeigt, wie diese Funktional ität verwendet wird:



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-pointcloud-EncodeSphereAsPointCloud-1.java" >}}
#  **Encodieren Sie Mesh auf PLY**
Aspose.3D for Java ermöglicht die direkte Codierung eines Netzes in PLY-Datei, ohne eine Szene mit der [`encode`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat#encode-com.aspose.threed.Entity-java.lang.String-)-Methode der [`PlyFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat)-Klasse zu erstellen. Das folgende Code-Snippet zeigt, wie diese Funktional ität verwendet wird:



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-pointcloud-EncodeMeshToPly-1.java" >}}
#  **Dekodieren Sie Mesh von PLY**
Aspose.3D for Java ermöglicht das Decodieren einer Mesh-/Punktwolke aus einer PLY-Datei mit der [`decode`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat#decode-java.lang.String-)-Methode der [`PlyFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat)-Klasse. Das folgende Code-Snippet zeigt, wie diese Funktional ität verwendet wird:



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-pointcloud-EncodeMeshToPly-1.java" >}}
#  **Als Point Cloud nach PLY exportieren**
Aspose.3D for Java ermöglicht den Export einer Szene nach PLY als Point Cloud mithilfe der [`encode`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat#encode-com.aspose.threed.Entity-java.lang.String-com.aspose.threed.PlySaveOptions-)-Methode der [`PlyFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat)-Klasse. Das folgende Code-Snippet zeigt, wie diese Funktional ität verwendet wird:



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-pointcloud-ExportToPlyAsPointCloud-1.java" >}}
#  **3D Szene als Point Cloud exportieren**
{{% alert color="primary" %}} 

Diese Funktion wird von Version 19.8 oder höher unterstützt.

{{% /alert %}} 

Aspose.3D for Java ermöglicht den Export einer 3D-Szene als Point Cloud mit der [`setPointCloud`](https://reference.aspose.com/3d/java/com.aspose.threed/ObjSaveOptions#setPointCloud-boolean-)-Methode der [`ObjSaveOptions`](https://reference.aspose.com/3d/java/com.aspose.threed/ObjSaveOptions)-Klasse. Das folgende Code-Snippet zeigt, wie diese Funktional ität verwendet wird:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-pointcloud-Export3DSceneAsPointCloud-1.java" >}}
