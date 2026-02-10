---
title: Generar datos normales para todas las mallas en un archivo 3D
type: docs
weight: 17
url: /es/net/generate-normal-data-for-all-meshes-in-a-3d-file/
description: Usando Aspose.3D for .NET, los desarrolladores pueden generar datos normales para todas las mallas en cualquier modelo 3D (sin los datos normales).
---
{{% alert color="primary" %}}

Usando [Aspose.3D for .NET](https://products.aspose.com/3d/net/), los desarrolladores pueden generar datos normales para todas las mallas en cualquier modelo 3D (sin los datos normales).

{{% /alert %}}
##  **Generar datos normales para todas las mallas en un archivo 3DS**
El método `GenerateNormal` expuesto por la clase [`PolygonModifier`](https://reference.aspose.com/3d/net/aspose.threed.entities/polygonmodifier) se puede usar para generar datos normales para todas las mallas en un archivo 3DS. Si el elemento `VertexElementSmoothingGroup` se definió en la malla, los datos normales generados serán suavizados por `VertexElementSmoothingGroup`.
###  **Muestra de programación**
Este ejemplo de código carga un archivo 3DS, visita todos los nodos y crea datos normales para todas las mallas.

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
