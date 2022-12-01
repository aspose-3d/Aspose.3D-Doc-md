---
title: Генерировать нормальные данные для всех сеток в файле 3D
type: docs
weight: 70
url: /ru/python-net/generate-normal-data-for-all-meshes-in-a-3d-file/
description: Используя Aspose.3D для Python via .NET, разработчики могут генерировать нормальные данные для всех сеток в любой модели 3D (без обычных данных).
---
{{% alert color="primary" %}}

Используя[Aspose.3D для Python via .NET](https://products.aspose.com/3d/python-net/), Разработчики могут генерировать нормальные данные для всех сеток в любой модели 3D (без нормальных данных).

{{% /alert %}}
## **Генерировать нормальные данные для всех сеток в файле 3DS**
Метод `generate_normal`, раскранный классом [`PolygonModifier`](https://reference.aspose.com/3d/net/aspose.threed.entities/polygonmodifier), может использоваться для генерации нормальных данных для всех сеток в файле 3DS. Если элемент `VertexElementSmoothingGroup` был определен в сетке, сгенерированные нормальные данные будут сглажены с помощью `VertexElementSmoothingGroup`.
### **Образец программирования**
Этот пример кода загружает файл 3DS, посещает все узлы и создает нормальные данные для всех сеток.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-GenerateDataForMeshes-GenerateDataForMeshes.py" >}}
