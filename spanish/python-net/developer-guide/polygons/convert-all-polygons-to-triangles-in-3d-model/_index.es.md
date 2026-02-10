---
title: Convertir todos los polígonos a triángulos en el modelo 3D
type: docs
weight: 10
url: /es/python-net/convert-all-polygons-to-triangles-in-3d-model/
description: Usando Aspose.3D for Python via .NET API, los desarrolladores pueden convertir todos los polígonos en triángulos en cualquier archivo 3D compatible.
---
{{% alert color="primary" %}}

Usando [Aspose.3D for Python via .NET](http://products.aspose.com/3d/net) API, los desarrolladores pueden convertir todos los polígonos en triángulos en cualquier archivo 3D compatible.

{{% /alert %}}
##  **Convertir todos los polígonos a triángulos**
Hemos agregado otra sobrecarga del método `triangulate` en la clase [`PolygonModifier`](https://reference.aspose.com/3d/net/aspose.threed.entities/polygonmodifier) que toma un objeto de clase [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) como parámetro como se muestra en este ejemplo de código:

{{< highlight "python" >}}
from aspose.threed import FileFormat, Scene
from aspose.threed.entities import PolygonModifier

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Load an existing 3D file
scene = Scene("data-dir"  + "document.fbx")
#  Triangulate a scene
PolygonModifier.triangulate(scene)
#  Save 3D scene
scene.save("out"  + "triangulated_out.fbx", FileFormat.FBX7400ASCII)

{{< /highlight >}}
