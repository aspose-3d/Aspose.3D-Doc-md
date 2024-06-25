---
title: Travailler avec PointCloud
type: docs
weight: 110
url: /fr/java/working-with-pointcloud/
description: Aspose.3D for Java permet de décoder un maillage à partir d'un fichier Draco directement sans construire une scène en utilisant la méthode de décodage de la classe DracoFormat.
---
#  **Décoder la maille**
Aspose.3D for Java permet de décoder un maillage à partir d'un fichier Draco directement sans construire de scène en utilisant la méthode [`decode`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat#decode-java.lang.String-) de la classe [`DracoFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat). L'extrait de code suivant montre comment utiliser cette fonctionnalité:



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-pointcloud-DecodeMesh-1.java" >}}
#  **Encode Mesh**
Aspose.3D for Java permet de coder directement un maillage de sphère dans un fichier Draco sans construire de scène en utilisant la méthode [`encode`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat#encode-com.aspose.threed.Entity-java.lang.String-) de la classe [`DracoFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat). L'extrait de code suivant montre comment utiliser cette fonctionnalité:



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-pointcloud-EncodeMesh-1.java" >}}
#  **Encoder la sphère en tant que PointCloud**
Aspose.3D for Java permet d'encoder un maillage de sphère dans un fichier Draco en tant que nuage de points en utilisant la méthode [`encode`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat#encode-com.aspose.threed.Entity-java.lang.String-com.aspose.threed.DracoSaveOptions-) de la classe [`DracoFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat). L'extrait de code suivant montre comment utiliser cette fonctionnalité:



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-pointcloud-EncodeSphereAsPointCloud-1.java" >}}
#  **Encoder le maillage à PLY**
Aspose.3D for Java permet d'encoder un maillage dans un fichier PLY directement sans construire de scène en utilisant la méthode [`encode`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat#encode-com.aspose.threed.Entity-java.lang.String-) de la classe [`PlyFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat). L'extrait de code suivant montre comment utiliser cette fonctionnalité:



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-pointcloud-EncodeMeshToPly-1.java" >}}
#  **Décoder le maillage à partir de PLY**
Aspose.3D for Java permet de décoder un maillage/nuage de points à partir d'un fichier PLY en utilisant la méthode [`decode`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat#decode-java.lang.String-) de la classe [`PlyFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat). L'extrait de code suivant montre comment utiliser cette fonctionnalité:



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-pointcloud-EncodeMeshToPly-1.java" >}}
#  **Exporter vers PLY en tant que PointCloud**
Aspose.3D for Java permet d'exporter une scène vers PLY en tant que PointCloud en utilisant la méthode [`encode`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat#encode-com.aspose.threed.Entity-java.lang.String-com.aspose.threed.PlySaveOptions-) de la classe [`PlyFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat). L'extrait de code suivant montre comment utiliser cette fonctionnalité:



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-pointcloud-ExportToPlyAsPointCloud-1.java" >}}
#  **Exporter 3D Scène sous forme de nuage de points**
{{% alert color="primary" %}} 

Cette fonctionnalité est prise en charge par la version 19.8 ou supérieure.

{{% /alert %}} 

Aspose.3D for Java permet d'exporter une scène 3D en tant que PointCloud en utilisant la méthode [`setPointCloud`](https://reference.aspose.com/3d/java/com.aspose.threed/ObjSaveOptions#setPointCloud-boolean-) de la classe [`ObjSaveOptions`](https://reference.aspose.com/3d/java/com.aspose.threed/ObjSaveOptions). L'extrait de code suivant montre comment utiliser cette fonctionnalité:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-pointcloud-Export3DSceneAsPointCloud-1.java" >}}
