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

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Working-with-Objects-GenerateDataForMeshes-GenerateDataForMeshes.cs" >}}
