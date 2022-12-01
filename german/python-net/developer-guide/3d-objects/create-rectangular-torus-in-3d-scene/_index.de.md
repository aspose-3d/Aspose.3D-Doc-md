---
title: Erstellen Sie rechteckige Torus in der Szene 3D
type: docs
weight: 50
url: /de/python-net/create-rectangular-torus-in-3d-scene/
description: Mithilfe von Aspose.3D für Python via .NET APIkönnen Entwickler 3D-Objekte erstellen und dann die 3D-Szene in einem beliebigen unterstützten 3D-Format speichern.
---
{{% alert color="primary" %}} 

Verwendung[Aspose.3D für Python via .NET](https://products.aspose.com/3d/python-net/)API können Entwickler 3D Objekte erstellen und dann die 3D-Szene in einem beliebigen unterstützten 3D-Format speichern.

{{% /alert %}} 
## **Rechteckiger Torus**
Wir haben die `RectangularTorus`-Klasse hinzugefügt, mit der Entwickler einen param etrisierten rechteckigen Torus in die Szene einbauen können. Dies kann in ein Ordnungsnetz/Dreiecks netz umgewandelt werden, während die Szene in verschiedene unterstützte Dateiformate gespeichert wird.

**Python**

```py

import math
from aspose.threed.entities import RectangularTorus

rt = RectangularTorus()

rt.inner_radius = 17

rt.outer_radius = 22

rt.height = 30

rt.arc = math.pi * 0.5

scene = Scene()

scene.root_node.create_child_node(rt)

scene.save("rtorus.obj", FileFormat.WAVEFRONT_OBJ)

```

Der erzeugte rechteckige Torus sieht wie folgt aus:

![Todo: bild_Alt_Text](create-rectangular-torus-in-3d-scene_1.png)
