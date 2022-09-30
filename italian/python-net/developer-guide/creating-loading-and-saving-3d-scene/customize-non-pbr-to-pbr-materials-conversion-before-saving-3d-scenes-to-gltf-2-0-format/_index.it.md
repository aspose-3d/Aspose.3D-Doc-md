---
title: Personalizzare la conversione dei materiali da PBR a PBR prima di salvare le scene da 3D al formato 2.0 GLTF
type: docs
weight: 70
url: /it/python-net/customize-non-pbr-to-pbr-materials-conversion-before-saving-3d-scenes-to-gltf-2-0-format/
description: La classe Scena dello Aspose.3D API rappresenta una scena 3D. Gli sviluppatori possono già costruire una scena 3D aggiungendo varie entità. GLTF 2.0 supporta solo materiali PBR (rendering basato sulla fisica), Aspose.3D API converte internamente materiali non PBR in materiali PBR prima di esportare in GLTF 2.0.
---
{{% alert color="primary" %}} 

La classe [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) dello Aspose.3D API rappresenta una scena 3D. Gli sviluppatori possono già costruire una scena 3D aggiungendo varie entità. GLTF 2.0 supporta solo materiali PBR (Physically Based Rendering), Aspose.3D API converte internamente materiali non PBR in materiali PBR prima di esportare in GLTF 2.0 (i materiali nella scena rimarranno invariati durante l'esportazione) e gli sviluppatori possono fornire funzione di conversione personalizzata per sovrascrivere il comportamento predefinito.

{{% /alert %}} 
## **Conversione del materiale da non PBR a PBR**
Questo esempio di codice mostra come convertire il materiale in materiale PBR e quindi salvare la scena 3D nel formato GLTF:

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
