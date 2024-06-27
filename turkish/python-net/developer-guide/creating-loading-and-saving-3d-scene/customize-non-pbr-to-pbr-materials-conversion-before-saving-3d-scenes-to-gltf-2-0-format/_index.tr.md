---
title: Customize Non-PBR to PBR Materials Conversion before Saving 3D Scenes to GLTF 2.0 Format
type: docs
weight: 70
url: /tr/python-net/customize-non-pbr-to-pbr-materials-conversion-before-saving-3d-scenes-to-gltf-2-0-format/
description: The Scene class of the Aspose.3D API represents a 3D scene. Developers can already build a 3D scene by adding various entities. GLTF 2.0 only supports PBR (Physically Based Rendering) materials, Aspose.3D API internally converts non-PBR materials into PBR materials before exporting into GLTF 2.0.
---
{{% alert color="primary" %}} 

The [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) class of the Aspose.3D API represents a 3D scene. Developers can already build a 3D scene by adding various entities. GLTF 2.0 only supports PBR (Physically Based Rendering) materials, Aspose.3D API internally converts non-PBR materials into PBR materials before exporting into GLTF 2.0 (the materials in the scene will remain unchanged during the export), and the developers can provide custom convert function to override the default behavior.

{{% /alert %}} 
##  **Non-PBto to PBerial erial aterial erial onversion**
Bu kod örneği, malzemeyi pbr malzemesine nasıl dönüştüreceğinizi gösterir ve daha sonra 3D formatında GLTF görüntüsünü kaydeder:

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
