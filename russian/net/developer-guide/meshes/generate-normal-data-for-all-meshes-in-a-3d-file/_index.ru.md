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

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET

            // Load a 3ds file, 3ds file doesn't have normal data, but it has smoothing group
            Scene s = new Scene(RunExamples.GetDataFilePath("camera.3ds"));
            // Visit all nodes and create normal data for all meshes
            s.RootNode.Accept(delegate(Node n)
            {
                Mesh mesh = n.GetEntity<Mesh>();
                if (mesh != null)
                {
                    VertexElementNormal normals = PolygonModifier.GenerateNormal(mesh);
                    mesh.VertexElements.Add(normals);
                }
                return true;
            });

{{< /highlight >}}
