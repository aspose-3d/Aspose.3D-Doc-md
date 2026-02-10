---
title: Работа с PointCloud
type: docs
weight: 110
url: /ru/java/working-with-pointcloud/
description: Aspose.3D for Java позволяет декодировать сетку из Draco файла напрямую, без построения сцены, используя метод декодирования класса DracoFormat.
---
#  **Декодирование сетки**
Aspose.3D for Java позволяет декодировать сетку из Draco файла напрямую без построения сцены с использованием метода [`decode`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat#decode-java.lang.String-) класса [`DracoFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat). Следующий фрагмент кода показывает, как использовать эту функциональность:



{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java
PointCloud pointCloud = (PointCloud) FileFormat.DRACO.decode(RunExamples.getDataDir() + "point_cloud_no_qp.drc");

{{< /highlight >}}
#  **Кодировать сетку**
Aspose.3D for Java позволяет напрямую кодировать сетку сферы в Draco файл без построения сцены методом [`encode`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat#encode-com.aspose.threed.Entity-java.lang.String-) класса [`DracoFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat). Следующий фрагмент кода показывает, как использовать эту функциональность:



{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java
FileFormat.DRACO.encode(new Sphere(), RunExamples.getDataDir() + "sphere.drc");

{{< /highlight >}}
#  **Кодировать сферу как PointCloud**
Aspose.3D for Java позволяет кодировать сферическую сетку в Draco файл как облако точек, используя метод [`encode`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat#encode-com.aspose.threed.Entity-java.lang.String-com.aspose.threed.DracoSaveOptions-) класса [`DracoFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/DracoFormat). Следующий фрагмент кода показывает, как использовать эту функциональность:



{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java
DracoSaveOptions opt = new DracoSaveOptions();
opt.setPointCloud(true);
FileFormat.DRACO.encode(new Sphere(), RunExamples.getDataDir()+"sphere.drc", opt);

{{< /highlight >}}
#  **Кодировать сетку в PLY**
Aspose.3D for Java позволяет напрямую кодировать сетку в PLY файл без построения сцены методом [`encode`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat#encode-com.aspose.threed.Entity-java.lang.String-) класса [`PlyFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat). Следующий фрагмент кода показывает, как использовать эту функциональность:



{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java
FileFormat.PLY.encode(new Sphere(), RunExamples.getDataDir() + "sphere.ply");

{{< /highlight >}}
#  **Декодирование сетки от PLY**
Aspose.3D for Java позволяет декодировать облако ячеек/точек из файла PLY методом [`decode`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat#decode-java.lang.String-) класса [`PlyFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat). Следующий фрагмент кода показывает, как использовать эту функциональность:



{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java
FileFormat.PLY.encode(new Sphere(), RunExamples.getDataDir() + "sphere.ply");

{{< /highlight >}}
#  **Экспортировать в PLY как PointCloud**
Aspose.3D for Java позволяет экспортировать сцену в PLY как PointCloud, используя метод [`encode`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat#encode-com.aspose.threed.Entity-java.lang.String-com.aspose.threed.PlySaveOptions-) класса [`PlyFormat`](https://reference.aspose.com/3d/java/com.aspose.threed/PlyFormat). Следующий фрагмент кода показывает, как использовать эту функциональность:



{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java
PlySaveOptions opt = new PlySaveOptions();
opt.setPointCloud(true);
FileFormat.PLY.encode(new Sphere(),RunExamples.getDataDir() + "sphere.ply", opt);

{{< /highlight >}}
#  **Экспортировать сцену 3D как облако точек**
{{% alert color="primary" %}} 

Эта функция поддерживается версией 19,8 или выше.

{{% /alert %}} 

Aspose.3D for Java позволяет экспортировать сцену 3D как PointCloud, используя метод [`setPointCloud`](https://reference.aspose.com/3d/java/com.aspose.threed/ObjSaveOptions#setPointCloud-boolean-) из класса [`ObjSaveOptions`](https://reference.aspose.com/3d/java/com.aspose.threed/ObjSaveOptions). Следующий фрагмент кода показывает, как использовать эту функциональность:

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
