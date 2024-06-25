---
title: Triangulación de un polígono simple
type: docs
weight: 30
url: /es/net/triangulation-of-a-simple-polygon/
description: Usando Aspose.3D for .NET API, los desarrolladores pueden triangular un polígono simple. Cualquier polígono se puede dividir en triángulos. Todas las operaciones y cálculos para triángulos se pueden aplicar por partes al polígono.
---
{{% alert color="primary" %}}

Usando [Aspose.3D for .NET](https://products.aspose.com/3d/net/) API, los desarrolladores pueden triangular un polígono simple. Cualquier polígono se puede dividir en triángulos. Todas las operaciones y cálculos para triángulos se pueden aplicar por partes al polígono.

{{% /alert %}}
##  **Triangulando un polígono**
Los desarrolladores pueden elegir vértices de un área de polígono, y luego formar triángulos llamando al método `Triangulate` de la clase [`PolygonModifier`](https://reference.aspose.com/3d/net/aspose.threed.entities/polygonmodifier), cada uno de los formularios V{1}, V{i-1}, V{i} con el índice i yendo de 3 a n. Las clases `Vertex` y `PolygonCanvas` en el archivo `Triangulate/PolygonCanvas.cs` bajo la aplicación de demostración (nombre: Triangulate) demuestra la forma de triangular un polígono usando Aspose.3D API.

{{% alert color="primary" %}}

Hemos preparado un proyecto de demostración. Por favor refiérase a [Esta URL](https://github.com/aspose-3d/Aspose.3D-for-.NET/tree/master/Demos).

{{% /alert %}}
###  **Muestra de programación para triangulación**
En este ejemplo de código se seleccionan vértices de un área de polígono y, a continuación, se aplica un algoritmo para crear triángulos. Puede descargar el proyecto de trabajo completo de este ejemplo desde [Aquí](https://github.com/aspose-3d/Aspose.3D-for-.NET/).

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "TriangulationSimplePolygon-Triangulate-PolygonCanvas-TriangulationofaSimplePolygon.cs" >}}
