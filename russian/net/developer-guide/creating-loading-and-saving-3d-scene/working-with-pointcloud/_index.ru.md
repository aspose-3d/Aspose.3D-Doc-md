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



{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-WorkingWithPointCloud-DecodeMesh-1.cs" >}}
#  **Кодировать сетку**
Aspose.3D for .NET позволяет напрямую кодировать сетку сферы в Draco файл без построения сцены методом [`Encode`](https://reference.aspose.com/net/3d/aspose.threed.formats.dracoformat/encode/methods/2) класса [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat). Следующий фрагмент кода показывает, как использовать эту функциональность:



{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-WorkingWithPointCloud-EncodeMesh-1.cs" >}}
#  **Кодировать сферу как PointCloud**
Aspose.3D for .NET позволяет кодировать сферическую сетку в Draco файл как облако точек, используя метод [`Encode`](https://reference.aspose.com/net/3d/aspose.threed.formats.dracoformat/encode/methods/2) класса [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat). Следующий фрагмент кода показывает, как использовать эту функциональность:



{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-WorkingWithPointCloud-EncodeSphereAsPointCloud-1.cs" >}}
#  **Кодировать сетку в PLY**
Aspose.3D for .NET позволяет напрямую кодировать сетку в PLY файл без построения сцены методом [`Encode`](https://reference.aspose.com/net/3d/aspose.threed.formats.plyformat/encode/methods/1) класса [`PlyFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/plyformat). Следующий фрагмент кода показывает, как использовать эту функциональность:



{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-WorkingWithPointCloud-EncodeMeshToPly-1.cs" >}}
#  **Декодирование сетки от PLY**
Aspose.3D for .NET позволяет декодировать облако ячеек/точек из файла PLY методом [`Decode`](https://reference.aspose.com/net/3d/aspose.threed.formats.plyformat/decode/methods/1) класса [`PlyFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/plyformat). Следующий фрагмент кода показывает, как использовать эту функциональность:



{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-WorkingWithPointCloud-EncodeMeshToPly-1.cs" >}}
#  **Экспортировать в PLY как PointCloud**
Aspose.3D for .NET позволяет экспортировать сцену в PLY как PointCloud, используя метод [`Encode`](https://reference.aspose.com/net/3d/aspose.threed.formats.plyformat/encode/methods/1) класса [`PlyFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/plyformat). Следующий фрагмент кода показывает, как использовать эту функциональность:



{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-WorkingWithPointCloud-ExportToPlyAsPointCloud-1.cs" >}}
#  **Экспортировать сцену 3D как облако точек**
{{% alert color="primary" %}} 

Эта функция поддерживается версией 19,8 или выше.

{{% /alert %}} 

Aspose.3D for .NET позволяет экспортировать сцену 3D как PointCloud, используя свойство [`PointCloud`](https://reference.aspose.com/net/3d/aspose.threed.formats/objsaveoptions/properties/pointcloud) класса [`ObjSaveOptions`](https://reference.aspose.com/net/3d/aspose.threed.formats/objsaveoptions). Следующий фрагмент кода показывает, как использовать эту функциональность:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-WorkingWithPointCloud-Export3DSceneAsPointCloud-1.cs" >}}
