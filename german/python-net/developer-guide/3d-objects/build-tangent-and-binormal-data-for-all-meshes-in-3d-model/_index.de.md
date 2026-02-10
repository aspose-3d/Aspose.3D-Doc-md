---
title: Erstellen Sie Tangenten-und Binormal daten für alle Maschen im 3D-Modell
type: docs
weight: 10
url: /de/python-net/build-tangent-and-binormal-data-for-all-meshes-in-3d-model/
description: Mit Aspose.3D for Python via .NET API können Entwickler tangente und binormale Daten für alle Netze in jeder unterstützten 3D-Datei erstellen.
---
{{% alert color="primary" %}}

Mit [Aspose.3D for Python via .NET](http://products.aspose.com/3d/net) API können Entwickler tangente und binormale Daten für alle Netze in jeder unterstützten 3D-Datei erstellen.

{{% /alert %}}
##  **Tangent-und Binormal-Daten für Mesh erstellen**
Wir haben zwei Build Tangentbinormal-Methoden in der [`PolygonModifier`](https://reference.aspose.com/3d/net/aspose.threed.entities/polygonmodifier)-Klasse hinzugefügt. Eine Methode verwendet das [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene)-Klassen objekt als Parameter und eine andere Methode das [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh)-Klassen objekt als Parameter, wie in diesem Code beispiel gezeigt:

{{< highlight "python" >}}
from aspose.threed import FileFormat, Scene
from aspose.threed.entities import PolygonModifier

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Load an existing 3D file
scene = Scene("data-dir"  + "document.fbx")
#  Triangulate a scene
PolygonModifier.build_tangent_binormal(scene)
#  Save 3D scene
scene.save("out"  + "BuildTangentAndBinormalData_out.fbx", FileFormat.FBX7400ASCII)

{{< /highlight >}}
