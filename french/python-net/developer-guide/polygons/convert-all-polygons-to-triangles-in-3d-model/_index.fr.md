---
title: Convertir tous les polygones en triangles dans le modèle 3D
type: docs
weight: 10
url: /fr/python-net/convert-all-polygons-to-triangles-in-3d-model/
description: En utilisant Aspose.3D for Python via .NET API, les développeurs peuvent convertir tous les polygones en triangles dans n'importe quel fichier 3D pris en charge.
---
{{% alert color="primary" %}}

En utilisant [Aspose.3D for Python via .NET](http://products.aspose.com/3d/net) API, les développeurs peuvent convertir tous les polygones en triangles dans n'importe quel fichier 3D pris en charge.

{{% /alert %}}
##  **Convertir tous les polygones en Triangles**
Nous avons ajouté une autre surcharge de la méthode `triangulate` dans la classe [`PolygonModifier`](https://reference.aspose.com/3d/net/aspose.threed.entities/polygonmodifier) qui prend un objet de classe [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) comme paramètre comme indiqué dans cet exemple de code:

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
