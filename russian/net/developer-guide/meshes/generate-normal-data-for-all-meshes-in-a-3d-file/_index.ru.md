---
title: Генерировать нормальные данные для всех ячеек в файле 3D
type: docs
weight: 17
url: /ru/net/generate-normal-data-for-all-meshes-in-a-3d-file/
description: Используя Aspose.3D for .NET, разработчики могут генерировать нормальные данные для всех ячеек в любой модели 3D (без нормальных данных).
---
{{% alert color="primary" %}}

Используя [Aspose.3D for .NET](https://products.aspose.com/3d/net/), разработчики могут генерировать нормальные данные для всех ячеек в любой модели 3D (без нормальных данных).

{{% /alert %}}
##  **Генерировать нормальные данные для всех ячеек в файле 3DS**
Метод `GenerateNormal`, представленный классом [`PolygonModifier`](https://reference.aspose.com/3d/net/aspose.threed.entities/polygonmodifier), можно использовать для генерации нормальных данных для всех ячеек в файле 3DS. Если элемент `VertexElementSmoothingGroup` был определен в сетке, сгенерированные нормальные данные будут сглажены на `VertexElementSmoothingGroup`.
###  **Образец программирования**
Этот пример кода загружает файл 3DS, посещает все узлы и создает нормальные данные для всех ячеек.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Working-with-Objects-GenerateDataForMeshes-GenerateDataForMeshes.cs" >}}
