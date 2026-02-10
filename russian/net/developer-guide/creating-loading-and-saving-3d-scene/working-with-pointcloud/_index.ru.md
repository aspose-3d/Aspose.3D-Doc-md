---
title: Работа с PointCloud
type: docs
weight: 150
url: /ru/net/working-with-pointcloud/
description: Aspose.3D for .NET позволяет декодировать сетку из Draco файла напрямую без построения сцены с помощью метода Decode класса DracoFormat.
---
{{% alert color="primary" %}} 

Эта функция поддерживается версией 19,7 или выше.

{{% /alert %}} 
#  **Декодирование сетки**
Aspose.3D for .NET позволяет декодировать сетку из Draco файла напрямую без построения сцены с использованием метода [`Decode`](https://reference.aspose.com/net/3d/aspose.threed.formats.dracoformat/decode/methods/1) класса [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat). Следующий фрагмент кода показывает, как использовать эту функциональность:



{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
var pointCloud = (PointCloud)FileFormat.Draco.Decode("point_cloud_no_qp.drc");

{{< /highlight >}}
#  **Кодировать сетку**
Aspose.3D for .NET позволяет напрямую кодировать сетку сферы в Draco файл без построения сцены методом [`Encode`](https://reference.aspose.com/net/3d/aspose.threed.formats.dracoformat/encode/methods/2) класса [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat). Следующий фрагмент кода показывает, как использовать эту функциональность:



{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
FileFormat.Draco.Encode(new Sphere(), "sphere.drc");

{{< /highlight >}}
#  **Кодировать сферу как PointCloud**
Aspose.3D for .NET позволяет кодировать сферическую сетку в Draco файл как облако точек, используя метод [`Encode`](https://reference.aspose.com/net/3d/aspose.threed.formats.dracoformat/encode/methods/2) класса [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat). Следующий фрагмент кода показывает, как использовать эту функциональность:



{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
FileFormat.Draco.Encode(new Sphere(), "sphere.drc", new DracoSaveOptions() { PointCloud = true });

{{< /highlight >}}
#  **Кодировать сетку в PLY**
Aspose.3D for .NET позволяет напрямую кодировать сетку в PLY файл без построения сцены методом [`Encode`](https://reference.aspose.com/net/3d/aspose.threed.formats.plyformat/encode/methods/1) класса [`PlyFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/plyformat). Следующий фрагмент кода показывает, как использовать эту функциональность:



{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
FileFormat.PLY.Encode(new Sphere(), "sphere.ply");

{{< /highlight >}}
#  **Декодирование сетки от PLY**
Aspose.3D for .NET позволяет декодировать облако ячеек/точек из файла PLY методом [`Decode`](https://reference.aspose.com/net/3d/aspose.threed.formats.plyformat/decode/methods/1) класса [`PlyFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/plyformat). Следующий фрагмент кода показывает, как использовать эту функциональность:



{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
FileFormat.PLY.Encode(new Sphere(), "sphere.ply");

{{< /highlight >}}
#  **Экспортировать в PLY как PointCloud**
Aspose.3D for .NET позволяет экспортировать сцену в PLY как PointCloud, используя метод [`Encode`](https://reference.aspose.com/net/3d/aspose.threed.formats.plyformat/encode/methods/1) класса [`PlyFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/plyformat). Следующий фрагмент кода показывает, как использовать эту функциональность:



{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
FileFormat.PLY.Encode(new Sphere(), "sphere.ply", new PlySaveOptions() { PointCloud = true });


{{< /highlight >}}
#  **Экспортировать сцену 3D как облако точек**
{{% alert color="primary" %}} 

Эта функция поддерживается версией 19,8 или выше.

{{% /alert %}} 

Aspose.3D for .NET позволяет экспортировать сцену 3D как PointCloud, используя свойство [`PointCloud`](https://reference.aspose.com/net/3d/aspose.threed.formats/objsaveoptions/properties/pointcloud) класса [`ObjSaveOptions`](https://reference.aspose.com/net/3d/aspose.threed.formats/objsaveoptions). Следующий фрагмент кода показывает, как использовать эту функциональность:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
var scene = new Scene(new Sphere());
scene.Save("Export3DSceneAsPointCloud.obj", new ObjSaveOptions() { PointCloud = true });

{{< /highlight >}}
