---
title: Créer un torus rectangulaire dans 3D Scène
type: docs
weight: 50
url: /fr/python-net/create-rectangular-torus-in-3d-scene/
description: En utilisant Aspose.3D for Python via .NET API, les développeurs peuvent créer des objets 3D, puis enregistrer une scène 3D dans n'importe quel format 3D pris en charge.
---
{{% alert color="primary" %}} 

En utilisant [Aspose.3D for Python via .NET](https://products.aspose.com/3d/python-net/) API, les développeurs peuvent créer des objets 3D, puis enregistrer une scène 3D dans n'importe quel format 3D pris en charge.

{{% /alert %}} 
##  **Tore rectangulaire**
Nous avons ajouté la classe `RectangularTorus`, elle permet aux développeurs de placer un tore rectangulaire paramétré dans la scène, ce qui peut être converti en maillage ordinal/maillage triangulaire lors de l'enregistrement de la scène dans différents formats de fichiers pris en charge.

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

Le tore rectangulaire généré ressemble à ce qui suit:

! [Tout le monde: image_alt_text](create-rectangular-torus-in-3d-scene_1.png)
