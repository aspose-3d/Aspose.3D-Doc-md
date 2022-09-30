---
title: Generar datos normales para todas las mallas en un archivo 3D
type: docs
weight: 70
url: /es/python-net/generate-normal-data-for-all-meshes-in-a-3d-file/
description: Usando Aspose.3D para Python via .NET, los desarrolladores pueden generar datos normales para todas las mallas en cualquier modelo 3D (sin los datos normales).
---
{{% alert color="primary" %}}

Uso[Aspose.3D para Python via .NET](https://products.aspose.com/3d/python-net/), Los desarrolladores pueden generar datos normales para todas las mallas en cualquier modelo 3D (sin los datos normales).

{{% /alert %}}
## **Generar datos normales para todas las mallas en un archivo 3DS**
El método `generate_normal` expuesto por la clase [`PolygonModifier`](https://reference.aspose.com/3d/net/aspose.threed.entities/polygonmodifier) se puede utilizar para generar datos normales para todas las mallas en un archivo 3DS. Si se definió el elemento `VertexElementSmoothingGroup` en la malla, el `VertexElementSmoothingGroup` suavizará los datos normales generados.
### **Muestra de programación**
Este ejemplo de código carga un archivo 3DS, visita todos los nodos y crea datos normales para todas las mallas.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-GenerateDataForMeshes-GenerateDataForMeshes.py" >}}
