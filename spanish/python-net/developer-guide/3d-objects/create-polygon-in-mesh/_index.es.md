---
title: Crear polígono en malla
type: docs
weight: 40
url: /es/python-net/create-polygon-in-mesh/
description: Aspose.3D for Python via .NET permite crear un polígono en una malla. Para usar la funcionalidad, el API ofrece el método CreatePolygon de la clase Mesh.
---
{{% alert color="primary" %}} 

Esta característica es compatible con la versión 19,8 o superior.

{{% /alert %}} 
##  **Crear polígono en malla**
Aspose.3D for Python via .NET permite crear un polígono en una malla. Para usar la funcionalidad, el API ofrece el método [`create_polygon`](https://reference.aspose.com/net/3d/aspose.threed.entities/mesh/methods/createpolygon) de la clase [`Mesh`](https://reference.aspose.com/net/3d/aspose.threed.entities/mesh). Usando el método `create_polygon` puede crear un polígono [Triángulo](https://reference.aspose.com/net/3d/aspose.threed.entities/mesh/methods/createpolygon)o [Cuádruple](https://reference.aspose.com/net/3d/aspose.threed.entities.mesh/createpolygon/methods/1) optimizado sin asignar memoria adicional. El siguiente fragmento de código muestra cómo utilizar esta funcionalidad.

{{< highlight "python" >}}
from aspose.threed.entities import Mesh

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
mesh = Mesh()
mesh.create_polygon([0, 1, 2 ])
mesh.create_polygon(0, 1, 2)

{{< /highlight >}}
