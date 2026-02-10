---
title: Mit Point Cloud arbeiten
type: docs
weight: 110
url: /de/java/working-with-pointcloud/
description: Aspose.3D for Java ermöglicht das direkte Decodieren eines Netzes aus einer Draco-Datei, ohne eine Szene mit der Dekodierung methode der DracoFormat-Klasse zu erstellen.
---
#  **Netz entschlüsseln**
Aspose.3D for Java ermöglicht das direkte Decodieren eines Netzes aus einer Draco-Datei, ohne eine Szene mit der [`decode`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat#decode-java.lang.String-)-Methode der [`DracoFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat)-Klasse zu erstellen. Das folgende Code-Snippet zeigt, wie diese Funktional ität verwendet wird:



{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java
PointCloud pointCloud = (PointCloud) FileFormat.DRACO.decode(RunExamples.getDataDir() + "point_cloud_no_qp.drc");

{{< /highlight >}}
#  **Maschen kodieren**
Aspose.3D for Java ermöglicht die direkte Codierung eines Kugel netzes in eine Draco-Datei, ohne eine Szene mit der [`encode`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat#encode-com.aspose.threed.Entity-java.lang.String-)-Methode der [`DracoFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat)-Klasse zu erstellen. Das folgende Code-Snippet zeigt, wie diese Funktional ität verwendet wird:



{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java
FileFormat.DRACO.encode(new Sphere(), RunExamples.getDataDir() + "sphere.drc");

{{< /highlight >}}
#  **Kugel als Point Cloud codieren**
Aspose.3D for Java ermöglicht das Codieren eines Kugel netzes in Draco-Datei als Punktwolke mit der [`encode`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat#encode-com.aspose.threed.Entity-java.lang.String-com.aspose.threed.DracoSaveOptions-)-Methode der [`DracoFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat)-Klasse. Das folgende Code-Snippet zeigt, wie diese Funktional ität verwendet wird:



{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java
DracoSaveOptions opt = new DracoSaveOptions();
opt.setPointCloud(true);
FileFormat.DRACO.encode(new Sphere(), RunExamples.getDataDir()+"sphere.drc", opt);

{{< /highlight >}}
#  **Encodieren Sie Mesh auf PLY**
Aspose.3D for Java ermöglicht die direkte Codierung eines Netzes in PLY-Datei, ohne eine Szene mit der [`encode`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat#encode-com.aspose.threed.Entity-java.lang.String-)-Methode der [`PlyFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat)-Klasse zu erstellen. Das folgende Code-Snippet zeigt, wie diese Funktional ität verwendet wird:



{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java
FileFormat.PLY.encode(new Sphere(), RunExamples.getDataDir() + "sphere.ply");

{{< /highlight >}}
#  **Dekodieren Sie Mesh von PLY**
Aspose.3D for Java ermöglicht das Decodieren einer Mesh-/Punktwolke aus einer PLY-Datei mit der [`decode`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat#decode-java.lang.String-)-Methode der [`PlyFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat)-Klasse. Das folgende Code-Snippet zeigt, wie diese Funktional ität verwendet wird:



{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java
FileFormat.PLY.encode(new Sphere(), RunExamples.getDataDir() + "sphere.ply");

{{< /highlight >}}
#  **Als Point Cloud nach PLY exportieren**
Aspose.3D for Java ermöglicht den Export einer Szene nach PLY als Point Cloud mithilfe der [`encode`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat#encode-com.aspose.threed.Entity-java.lang.String-com.aspose.threed.PlySaveOptions-)-Methode der [`PlyFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat)-Klasse. Das folgende Code-Snippet zeigt, wie diese Funktional ität verwendet wird:



{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java
PlySaveOptions opt = new PlySaveOptions();
opt.setPointCloud(true);
FileFormat.PLY.encode(new Sphere(),RunExamples.getDataDir() + "sphere.ply", opt);

{{< /highlight >}}
#  **3D Szene als Point Cloud exportieren**
{{% alert color="primary" %}} 

Diese Funktion wird von Version 19.8 oder höher unterstützt.

{{% /alert %}} 

Aspose.3D for Java ermöglicht den Export einer 3D-Szene als Point Cloud mit der [`setPointCloud`](https://reference.aspose.com/3d/java/com.aspose.threed/ObjSaveOptions#setPointCloud-boolean-)-Methode der [`ObjSaveOptions`](https://reference.aspose.com/3d/java/com.aspose.threed/ObjSaveOptions)-Klasse. Das folgende Code-Snippet zeigt, wie diese Funktional ität verwendet wird:

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
