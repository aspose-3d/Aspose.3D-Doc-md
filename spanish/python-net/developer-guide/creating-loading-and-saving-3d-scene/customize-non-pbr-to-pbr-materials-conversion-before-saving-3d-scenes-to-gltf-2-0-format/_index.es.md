---
title: Personalizar la conversión de materiales no PBR a PBR antes de guardar las escenas 3D en formato GLTF 2,0
type: docs
weight: 70
url: /es/python-net/customize-non-pbr-to-pbr-materials-conversion-before-saving-3d-scenes-to-gltf-2-0-format/
description: La clase Escena del Aspose.3D API representa una escena 3D. Los desarrolladores ya pueden construir una escena 3D agregando varias entidades. GLTF 2,0 solo admite materiales PBR (Rendering Físicamente Based), Aspose.3D API convierte internamente materiales que no son PBR en materiales PBR antes de exportarlos a GLTF 2,0.
---
{{% alert color="primary" %}} 

La clase [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) del Aspose.3D API representa una escena 3D. Los desarrolladores ya pueden construir una escena 3D agregando varias entidades. GLTF 2,0 solo admite materiales PBR (Rendering Físicamente Based), Aspose.3D API convierte internamente materiales que no son PBR en materiales PBR antes de exportar a GLTF 2,0 (los materiales en la escena permanecerán sin cambios durante la exportación), y los desarrolladores pueden proporcionar una función de conversión personalizada para anular el comportamiento predeterminado.

{{% /alert %}} 
## **Conversión de material no PBR a PBR**
Este ejemplo de código muestra cómo convertir material a material PBR y, a continuación, guarda la escena 3D en formato GLTF:

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
