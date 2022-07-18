---
title: Triangulation of a Simple Polygon
type: docs
weight: 30
url: /python-net/triangulation-of-a-simple-polygon/
description: Using Aspose.3D for Python via .NET API, developers can triangulate a simple polygon. Any polygon can be divided into triangles. All of the operations and calculations for triangles can be piecewise applied to the polygon.
---

{{% alert color="primary" %}}

Using [Aspose.3D for Python via .NET](https://products.aspose.com/3d/python-net/) API, developers can triangulate a simple polygon. Any polygon can be divided into triangles. All of the operations and calculations for triangles can be piecewise applied to the polygon.

{{% /alert %}}
## **Triangulating a Polygon**
Developers might pick vertices from a polygon area, and then form triangles by calling Triangulate method of the [PolygonModifier](https://reference.aspose.com/3d/python-net/aspose.threed.entities/polygonmodifier) class, each of the form V{1}, V{i-1}, V{i} with the index i going from 3 to n. The Vertex and PolygonCanvas classes in **Triangulate/PolygonCanvas.py** file under the demo application (name:Triangulate) demonstrates the way of triangulating a polygon using Aspose.3D API.

{{% alert color="primary" %}}

We have prepared a demo project. Please refer to [this URL](https://github.com/aspose-3d/Aspose.3D-for-.NET/tree/master/Demos).

{{% /alert %}}
### **Programming Sample for Triangulation**
This code example picks vertices from a polygon area, and then apply an algorithm to create triangles. You can download complete working project of this example from [here](https://github.com/aspose-3d/Aspose.3D-for-.NET/).

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "TriangulationSimplePolygon-Triangulate-PolygonCanvas-TriangulationofaSimplePolygon.py" >}}
