---
title : "Triangulation of a Simple Polygon" 
description : "" 
weight : 12067 
toc : false
type: docs
url: /net/developerguide/polygons/triangulation+of+a+simple+polygon/
---

# Aspose.3D for .NET : Triangulation of a Simple Polygon


Using [Aspose.3D for .NET](http://www.aspose.com/3d-component-suite.aspx) API, developers can triangulate a simple polygon. Any polygon can be divided into triangles. All of the operations and calculations for triangles can be piecewise applied to the polygon.

## Triangulating a Polygon

Developers might pick vertices from a polygon area, and then form triangles by calling `Triangulate` method of the [PolygonModifier](http://www.aspose.com/api/net/3d/aspose.threed.entities/polygonmodifier) class, each of the form V{1}, V{i-1}, V{i} with the index i going from 3 to n. The Vertex and PolygonCanvas classes in **Triangulate/PolygonCanvas.cs** file under the demo application (name:Triangulate) demonstrates the way of triangulating a polygon using Aspose.3D API.

We have prepared a demo project. Please refer to [this download URL](https://github.com/aspose-3d/Aspose.3D-for-.NET/tree/master/TriangulationSimplePolygon).

### Programming Sample for Triangulation

This code example picks vertices from a polygon area, and then apply an algorithm to create triangles. You can download complete working project of this example from [here](https://github.com/aspose-3d/Aspose.3D-for-.NET/tree/master/TriangulationSimplePolygon).

