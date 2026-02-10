---
title: Convertire tutti i poligoni in triangoli nel modello 3D
type: docs
weight: 10
url: /it/python-net/convert-all-polygons-to-triangles-in-3d-model/
description: Utilizzando Aspose.3D for Python via .NET API, gli sviluppatori possono convertire tutti i poligoni in triangoli in qualsiasi file 3D supportato.
---
{{% alert color="primary" %}}

Utilizzando [Aspose.3D for Python via .NET](http://products.aspose.com/3d/net) API, gli sviluppatori possono convertire tutti i poligoni in triangoli in qualsiasi file 3D supportato.

{{% /alert %}}
##  **Convertire tutti i poligoni a triangoli**
Abbiamo aggiunto un altro overload di `triangulate` nella classe [`PolygonModifier`](https://reference.aspose.com/3d/net/aspose.threed.entities/polygonmodifier) che accetta un oggetto di classe [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) come parametro, come mostrato in questo esempio di codice:

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
