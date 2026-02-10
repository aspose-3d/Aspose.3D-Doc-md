---
title: Crear polígono en malla
type: docs
weight: 14
url: /es/net/create-polygon-in-mesh/
description: Aspose.3D for .NET permite crear un polígono en una malla. Para usar la funcionalidad, API ofrece el método CreatePolygon de la clase Mesh.
---
{{% alert color="primary" %}} 

Esta característica es compatible con la versión 19,8 o superior.

{{% /alert %}} 
##  **Crear polígono en malla**
Aspose.3D for .NET permite crear un polígono en una malla. Para usar la funcionalidad, el API ofrece el método [`CreatePolygon`](https://reference.aspose.com/net/3d/aspose.threed.entities/mesh/methods/createpolygon) de la clase [`Mesh`](https://reference.aspose.com/net/3d/aspose.threed.entities/mesh). Usando el método CreatePolygon puede crear un polígono [Triángulo](https://reference.aspose.com/net/3d/aspose.threed.entities/mesh/methods/createpolygon)o [Cuádruple](https://reference.aspose.com/net/3d/aspose.threed.entities.mesh/createpolygon/methods/1) optimizado sin asignar memoria adicional. El siguiente fragmento de código muestra cómo utilizar esta funcionalidad.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
Mesh mesh = new Mesh();
mesh.CreatePolygon(new int[] { 0, 1, 2 }); //The old CreatePolygon needs to create a temporary array for holding the face indices
mesh.CreatePolygon(0, 1, 2); //The new overloads doesn't need extra allocation, and it's optimized internally.

//Or You can create a polygon using 4 vertices(quad)
//mesh.CreatePolygon(0, 1, 2, 3);

{{< /highlight >}}
