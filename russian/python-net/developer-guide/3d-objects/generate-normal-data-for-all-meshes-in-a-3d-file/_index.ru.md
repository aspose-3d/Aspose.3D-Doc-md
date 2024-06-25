---
title: Генерировать нормальные данные для всех ячеек в файле 3D
type: docs
weight: 70
url: /ru/python-net/generate-normal-data-for-all-meshes-in-a-3d-file/
description: Используя Aspose.3D for Python via .NET, разработчики могут генерировать нормальные данные для всех ячеек в любой модели 3D (без нормальных данных).
---
{{% alert color="primary" %}}

Используя [Aspose.3D for Python via .NET](https://products.aspose.com/3d/python-net/), разработчики могут генерировать нормальные данные для всех ячеек в любой модели 3D (без нормальных данных).

{{% /alert %}}
##  **Генерировать нормальные данные для всех ячеек в файле 3DS**
Метод `generate_normal`, представленный классом [`PolygonModifier`](https://reference.aspose.com/3d/net/aspose.threed.entities/polygonmodifier), можно использовать для генерации нормальных данных для всех ячеек в файле 3DS. Если элемент `VertexElementSmoothingGroup` был определен в сетке, сгенерированные нормальные данные будут сглажены на `VertexElementSmoothingGroup`.
###  **Образец программирования**
Этот пример кода загружает файл 3DS, посещает все узлы и создает нормальные данные для всех ячеек.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-GenerateDataForMeshes-GenerateDataForMeshes.py" >}}
