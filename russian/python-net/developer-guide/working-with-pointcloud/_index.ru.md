---
title: Работа с PointCloud
type: docs
weight: 150
url: /ru/python-net/working-with-pointcloud/
description: Aspose.3D для Python via .NET позволяет декодировать сетку из файла Draco напрямую без построения сцены с использованием метода Decode класса DracoFormat.
---
{{% alert color="primary" %}} 

Эта функция поддерживается версией 19,7 или выше.

{{% /alert %}} 
# **Декодирование сетки**
Aspose.3D для Python via .NET позволяет декодировать сетку из файла Draco напрямую без построения сцены с использованием метода [`decode`](https://reference.aspose.com/python/3d/aspose.threed.formats.dracoformat/decode/methods/1) класса [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat). Следующий фрагмент кода показывает, как использовать эту функциональность:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithPointCloud-DecodeMesh-1.py" >}}
# **Кодировать сетку**
Aspose.3D для Python via .NET позволяет напрямую кодировать сферную сетку в файл Draco без построения сцены с использованием метода [`encode`](https://reference.aspose.com/python/3d/aspose.threed.formats.dracoformat/encode/methods/2) класса [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat). Следующий фрагмент кода показывает, как использовать эту функциональность:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithPointCloud-EncodeMesh-1.py" >}}
# **Кодировать сферу как PointCloud**
Aspose.3D для Python via .NET позволяет кодировать сферную сетку в файл Draco как облако точек с использованием метода [`encode`](https://reference.aspose.com/python-net/3d/aspose.threed.formats.dracoformat/encode/methods/2) класса [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat). Следующий фрагмент кода показывает, как использовать эту функциональность:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithPointCloud-EncodeSphereAsPointCloud-1.py" >}}
# **Кодировать сетку к PLY**
Aspose.3D для Python via .NET позволяет напрямую кодировать файл сетки в файл PLY без создания сцены с помощью[Код](https://reference.aspose.com/python-net/3d/aspose.threed.formats.plyformat/encode/methods/1)Метод[Формат PlyFormat](https://reference.aspose.com/net/3d/aspose.threed.formats/plyformat)Класс. Следующий фрагмент кода показывает, как использовать эту функциональность:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithPointCloud-EncodeMeshToPly-1.py" >}}
# **Декодировать Mesh от PLY**
Aspose.3D для Python via .NET позволяет декодировать облако сетки/точек из файла PLY с использованием метода [`decode`](https://reference.aspose.com/python-net/3d/aspose.threed.formats.plyformat/decode/methods/1) класса [`PlyFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/plyformat). Следующий фрагмент кода показывает, как использовать эту функциональность:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithPointCloud-EncodeMeshToPly-1.py" >}}
# **Экспорт в PLY как PointCloud**
Aspose.3D для Python via .NET позволяет экспортировать сцену в PLY как PointCloud с использованием метода [`encode`](https://reference.aspose.com/python-net/3d/aspose.threed.formats.plyformat/encode/methods/1) класса [`PlyFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/plyformat). Следующий фрагмент кода показывает, как использовать эту функциональность:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithPointCloud-ExportToPlyAsPointCloud-1.py" >}}
# **Экспорт 3D Сцена в виде облака точек**
{{% alert color="primary" %}} 

Эта функция поддерживается версией 19,8 или выше.

{{% /alert %}} 

Aspose.3D для Python via .NET позволяет экспортировать сцену 3D как PointCloud с использованием свойства [`point_cloud`](https://reference.aspose.com/python-net/3d/aspose.threed.formats/objsaveoptions/properties/pointcloud) класса [`ObjSaveOptions`](https://reference.aspose.com/net/3d/aspose.threed.formats/objsaveoptions). Следующий фрагмент кода показывает, как использовать эту функциональность:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithPointCloud-Export3DSceneAsPointCloud-1.py" >}}
