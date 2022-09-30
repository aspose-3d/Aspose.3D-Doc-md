---
title: Créer Torus rectangulaire dans 3D Scène
type: docs
weight: 50
url: /fr/python-net/create-rectangular-torus-in-3d-scene/
description: En utilisant Aspose.3D pour Python via .NET API, les développeurs peuvent créer des objets 3D, puis enregistrer la scène 3D dans n'importe quel format 3D pris en charge.
---
{{% alert color="primary" %}} 

Utilisation[Aspose.3D pour Python via .NET](https://products.aspose.com/3d/python-net/)API, les développeurs peuvent créer des objets 3D, puis enregistrer la scène 3D dans n'importe quel format 3D pris en charge.

{{% /alert %}} 
## **Tore rectangulaire**
Nous avons ajouté la classe `RectangularTorus`, elle permet aux développeurs de placer un tore rectangulaire paramétré dans la scène, cela peut être converti en maillage ordinal/maillage triangle lors de l'enregistrement de la scène dans différents formats de fichiers pris en charge.

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

![Todo: image_Alt_Texte](create-rectangular-torus-in-3d-scene_1.png)
