---
title: Работа с PointCloud
type: docs
weight: 150
url: /ru/python-net/working-with-pointcloud/
description: Aspose.3D for Python via .NET позволяет декодировать сетку из Draco файла напрямую без построения сцены с использованием метода Decode класса DracoFormat.
---
{{% alert color="primary" %}} 

Эта функция поддерживается версией 19,7 или выше.

{{% /alert %}} 
#  **Декодирование сетки**
Aspose.3D for Python via .NET позволяет декодировать сетку из Draco файла напрямую без построения сцены с использованием метода [`decode`](https://reference.aspose.com/python/3d/aspose.threed.formats.dracoformat/decode/methods/1) класса [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat). Следующий фрагмент кода показывает, как использовать эту функциональность:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithPointCloud-DecodeMesh-1.py" >}}
#  **Кодировать сетку**
Aspose.3D for Python via .NET позволяет напрямую кодировать сетку сферы в Draco файл без построения сцены методом [`encode`](https://reference.aspose.com/python/3d/aspose.threed.formats.dracoformat/encode/methods/2) класса [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat). Следующий фрагмент кода показывает, как использовать эту функциональность:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithPointCloud-EncodeMesh-1.py" >}}
#  **Кодировать сферу как PointCloud**
Aspose.3D for Python via .NET позволяет кодировать сферическую сетку в Draco файл как облако точек, используя метод [`encode`](https://reference.aspose.com/python-net/3d/aspose.threed.formats.dracoformat/encode/methods/2) класса [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat). Следующий фрагмент кода показывает, как использовать эту функциональность:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithPointCloud-EncodeSphereAsPointCloud-1.py" >}}
#  **Кодировать сетку в PLY**
Aspose.3D for Python via .NET позволяет кодировать сетку в PLY файл напрямую без построения сцены с использованием метода [Код](https://reference.aspose.com/python-net/3d/aspose.threed.formats.plyformat/encode/methods/1) класса [Формат PlyFormat](https://reference.aspose.com/net/3d/aspose.threed.formats/plyformat). Следующий фрагмент кода показывает, как использовать эту функциональность:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithPointCloud-EncodeMeshToPly-1.py" >}}
#  **Декодирование сетки от PLY**
Aspose.3D for Python via .NET позволяет декодировать облако ячеек/точек из файла PLY методом [`decode`](https://reference.aspose.com/python-net/3d/aspose.threed.formats.plyformat/decode/methods/1) класса [`PlyFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/plyformat). Следующий фрагмент кода показывает, как использовать эту функциональность:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithPointCloud-EncodeMeshToPly-1.py" >}}
#  **Экспортировать в PLY как PointCloud**
Aspose.3D for Python via .NET позволяет экспортировать сцену в PLY как PointCloud, используя метод [`encode`](https://reference.aspose.com/python-net/3d/aspose.threed.formats.plyformat/encode/methods/1) класса [`PlyFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/plyformat). Следующий фрагмент кода показывает, как использовать эту функциональность:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithPointCloud-ExportToPlyAsPointCloud-1.py" >}}
#  **Экспортировать сцену 3D как облако точек**
{{% alert color="primary" %}} 

Эта функция поддерживается версией 19,8 или выше.

{{% /alert %}} 

Aspose.3D for Python via .NET позволяет экспортировать сцену 3D как PointCloud, используя свойство [`point_cloud`](https://reference.aspose.com/python-net/3d/aspose.threed.formats/objsaveoptions/properties/pointcloud) класса [`ObjSaveOptions`](https://reference.aspose.com/net/3d/aspose.threed.formats/objsaveoptions). Следующий фрагмент кода показывает, как использовать эту функциональность:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithPointCloud-Export3DSceneAsPointCloud-1.py" >}}
