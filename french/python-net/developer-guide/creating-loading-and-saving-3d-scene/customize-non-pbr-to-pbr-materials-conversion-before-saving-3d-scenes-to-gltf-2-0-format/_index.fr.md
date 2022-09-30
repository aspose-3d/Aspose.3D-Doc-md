---
title: Personnaliser la conversion de matériaux non-PBR en PBR avant de sauver les scènes 3D au format GLTF 2.0
type: docs
weight: 70
url: /fr/python-net/customize-non-pbr-to-pbr-materials-conversion-before-saving-3d-scenes-to-gltf-2-0-format/
description: La classe Scène du Aspose.3D API représente une scène 3D. Les développeurs peuvent déjà construire une scène 3D en ajoutant diverses entités. Le GLTF 2.0 prend uniquement en charge les matériaux PBR (rendu à base physique), le Aspose.3D API convertit en interne les matériaux non PBR en matériaux PBR avant l'exportation en GLTF 2.0.
---
{{% alert color="primary" %}} 

La classe [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) du Aspose.3D API représente une scène 3D. Les développeurs peuvent déjà construire une scène 3D en ajoutant diverses entités. GLTF 2.0 prend uniquement en charge les matériaux PBR (rendu à base physique), Aspose.3D API convertit en interne les matériaux non PBR en matériaux PBR avant d'exporter en GLTF 2.0 (les matériaux de la scène resteront inchangés pendant l'exportation), et les développeurs peuvent fournir une fonction de conversion personnalisée pour remplacer le comportement par défaut.

{{% /alert %}} 
## **Conversion de matériaux non-PBR vers PBR**
Cet exemple de code montre comment convertir du matériel en matériel PBR, puis enregistre la scène 3D au format GLTF:

**C#**

```py

import aspose.threed as a3d

# initialize a new 3D scene

s = a3d.Scene()

box = a3d.Box()

mat = a3d.shading.PhongMaterial()
mat.diffuse_color = Vector3(1, 0, 1)

s.root_node.create_child_node("box1", box).material = mat

opt = a3d.formats.GLTFSaveOptions(FileFormat.GLTF2);

# save in GLTF 2.0 format

s.save("test.gltf", opt);

```
