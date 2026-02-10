---
title: Travailler avec PointCloud
type: docs
weight: 110
url: /fr/java/working-with-pointcloud/
description: Aspose.3D for Java permet de décoder un maillage à partir d'un fichier Draco directement sans construire une scène en utilisant la méthode de décodage de la classe DracoFormat.
---
#  **Décoder la maille**
Aspose.3D for Java permet de décoder un maillage à partir d'un fichier Draco directement sans construire de scène en utilisant la méthode [`decode`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat#decode-java.lang.String-) de la classe [`DracoFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat). L'extrait de code suivant montre comment utiliser cette fonctionnalité:



{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java
PointCloud pointCloud = (PointCloud) FileFormat.DRACO.decode(RunExamples.getDataDir() + "point_cloud_no_qp.drc");

{{< /highlight >}}
#  **Encode Mesh**
Aspose.3D for Java permet de coder directement un maillage de sphère dans un fichier Draco sans construire de scène en utilisant la méthode [`encode`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat#encode-com.aspose.threed.Entity-java.lang.String-) de la classe [`DracoFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat). L'extrait de code suivant montre comment utiliser cette fonctionnalité:



{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java
FileFormat.DRACO.encode(new Sphere(), RunExamples.getDataDir() + "sphere.drc");

{{< /highlight >}}
#  **Encoder la sphère en tant que PointCloud**
Aspose.3D for Java permet d'encoder un maillage de sphère dans un fichier Draco en tant que nuage de points en utilisant la méthode [`encode`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat#encode-com.aspose.threed.Entity-java.lang.String-com.aspose.threed.DracoSaveOptions-) de la classe [`DracoFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat). L'extrait de code suivant montre comment utiliser cette fonctionnalité:



{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java
DracoSaveOptions opt = new DracoSaveOptions();
opt.setPointCloud(true);
FileFormat.DRACO.encode(new Sphere(), RunExamples.getDataDir()+"sphere.drc", opt);

{{< /highlight >}}
#  **Encoder le maillage à PLY**
Aspose.3D for Java permet d'encoder un maillage dans un fichier PLY directement sans construire de scène en utilisant la méthode [`encode`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat#encode-com.aspose.threed.Entity-java.lang.String-) de la classe [`PlyFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat). L'extrait de code suivant montre comment utiliser cette fonctionnalité:



{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java
FileFormat.PLY.encode(new Sphere(), RunExamples.getDataDir() + "sphere.ply");

{{< /highlight >}}
#  **Décoder le maillage à partir de PLY**
Aspose.3D for Java permet de décoder un maillage/nuage de points à partir d'un fichier PLY en utilisant la méthode [`decode`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat#decode-java.lang.String-) de la classe [`PlyFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat). L'extrait de code suivant montre comment utiliser cette fonctionnalité:



{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java
FileFormat.PLY.encode(new Sphere(), RunExamples.getDataDir() + "sphere.ply");

{{< /highlight >}}
#  **Exporter vers PLY en tant que PointCloud**
Aspose.3D for Java permet d'exporter une scène vers PLY en tant que PointCloud en utilisant la méthode [`encode`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat#encode-com.aspose.threed.Entity-java.lang.String-com.aspose.threed.PlySaveOptions-) de la classe [`PlyFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat). L'extrait de code suivant montre comment utiliser cette fonctionnalité:



{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java
PlySaveOptions opt = new PlySaveOptions();
opt.setPointCloud(true);
FileFormat.PLY.encode(new Sphere(),RunExamples.getDataDir() + "sphere.ply", opt);

{{< /highlight >}}
#  **Exporter 3D Scène sous forme de nuage de points**
{{% alert color="primary" %}} 

Cette fonctionnalité est prise en charge par la version 19.8 ou supérieure.

{{% /alert %}} 

Aspose.3D for Java permet d'exporter une scène 3D en tant que PointCloud en utilisant la méthode [`setPointCloud`](https://reference.aspose.com/3d/java/com.aspose.threed/ObjSaveOptions#setPointCloud-boolean-) de la classe [`ObjSaveOptions`](https://reference.aspose.com/3d/java/com.aspose.threed/ObjSaveOptions). L'extrait de code suivant montre comment utiliser cette fonctionnalité:

{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java
// Initialize Scene
Scene scene = new Scene(new Sphere());
// Initialize  ObjSaveOptions
ObjSaveOptions opt = new ObjSaveOptions();
// To export 3D scene as point cloud setPointCould
opt.setPointCloud(true);
// Save
scene.save(RunExamples.getDataDir()+ "export3DSceneAsPointCloud.obj", opt);

{{< /highlight >}}
