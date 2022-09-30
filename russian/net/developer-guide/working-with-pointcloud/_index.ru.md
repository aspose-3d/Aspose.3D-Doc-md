---
title: Работа с PointCloud
type: docs
weight: 150
url: /ru/net/working-with-pointcloud/
description: Aspose.3D for .NET позволяет напрямую декодировать сетку из файла Draco без построения сцены с использованием метода Decode класса DracoFormat.
---
{{% alert color="primary" %}} 

Эта функция поддерживается версией 19,7 или выше.

{{% /alert %}} 
# **Декодирование сетки**
Aspose.3D for .NET позволяет напрямую декодировать сетку из файла Draco без построения сцены с использованием метода [`Decode`](https://reference.aspose.com/net/3d/aspose.threed.formats.dracoformat/decode/methods/1) класса [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat). Следующий фрагмент кода показывает, как использовать эту функциональность:



{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-WorkingWithPointCloud-DecodeMesh-1.cs" >}}
# **Кодировать сетку**
Aspose.3D for .NET позволяет напрямую кодировать сферную сетку в файл Draco без создания сцены с использованием метода [`Encode`](https://reference.aspose.com/net/3d/aspose.threed.formats.dracoformat/encode/methods/2) класса [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat). Следующий фрагмент кода показывает, как использовать эту функциональность:



{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-WorkingWithPointCloud-EncodeMesh-1.cs" >}}
# **Кодировать сферу как PointCloud**
Aspose.3D for .NET позволяет кодировать сферную сетку в файл Draco как облако точек с использованием метода [`Encode`](https://reference.aspose.com/net/3d/aspose.threed.formats.dracoformat/encode/methods/2) класса [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat). Следующий фрагмент кода показывает, как использовать эту функциональность:



{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-WorkingWithPointCloud-EncodeSphereAsPointCloud-1.cs" >}}
# **Кодировать сетку к PLY**
Aspose.3D for .NET позволяет напрямую кодировать сетку в файл PLY без создания сцены с использованием метода [`Encode`](https://reference.aspose.com/net/3d/aspose.threed.formats.plyformat/encode/methods/1) класса [`PlyFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/plyformat). Следующий фрагмент кода показывает, как использовать эту функциональность:



{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-WorkingWithPointCloud-EncodeMeshToPly-1.cs" >}}
# **Декодировать Mesh от PLY**
Aspose.3D for .NET позволяет декодировать облако сетки/точек из файла PLY с использованием метода [`Decode`](https://reference.aspose.com/net/3d/aspose.threed.formats.plyformat/decode/methods/1) класса [`PlyFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/plyformat). Следующий фрагмент кода показывает, как использовать эту функциональность:



{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-WorkingWithPointCloud-EncodeMeshToPly-1.cs" >}}
# **Экспорт в PLY как PointCloud**
Aspose.3D for .NET позволяет экспортировать сцену в PLY как PointCloud с использованием метода [`Encode`](https://reference.aspose.com/net/3d/aspose.threed.formats.plyformat/encode/methods/1) класса [`PlyFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/plyformat). Следующий фрагмент кода показывает, как использовать эту функциональность:



{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-WorkingWithPointCloud-ExportToPlyAsPointCloud-1.cs" >}}
# **Экспорт 3D Сцена в виде облака точек**
{{% alert color="primary" %}} 

Эта функция поддерживается версией 19,8 или выше.

{{% /alert %}} 

Aspose.3D for .NET позволяет экспортировать сцену 3D как PointCloud с использованием свойства [`PointCloud`](https://reference.aspose.com/net/3d/aspose.threed.formats/objsaveoptions/properties/pointcloud) класса [`ObjSaveOptions`](https://reference.aspose.com/net/3d/aspose.threed.formats/objsaveoptions). Следующий фрагмент кода показывает, как использовать эту функциональность:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-WorkingWithPointCloud-Export3DSceneAsPointCloud-1.cs" >}}
