---
title: Anpassa icke-PBR till PBR material konvertering innan Spara 3D Scener till GLTF 2.0 Format
type: docs
weight: 70
url: /sv/python-net/customize-non-pbr-to-pbr-materials-conversion-before-saving-3d-scenes-to-gltf-2-0-format/
description: Scenklassen av Aspose.3D API representerar en 3D scen. Utvecklare kan redan bygga en 3D scen genom att lägga till olika enheter. GLTF 2.0 stöder endast PBR-material (Fysiskt baserad rendering). Aspose.3D API internt omvandlar icke-PBR-material till PBR-material före export till GLTF 2,0 ..
---
{{% alert color="primary" %}} 

Klassen [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) Aspose.3D API representerar en 3D scen. Utvecklare kan redan bygga en 3D scen genom att lägga till olika enheter. GLTF 2.0 stöder endast PBR-material (Fysiskt baserad rendering). Aspose.3D API internt omvandlar icke-PBR-material till PBR-material före export till GLTF 2,0 (materialet i scenen kommer att förbli oförändrat under exporten), och utvecklarna kan ge anpassad konvertera funktion för att åsidosätta standardben Beteende.

{{% /alert %}} 
## **Omvandling av material som inte omfattas av PBR till PBR**
Detta kodexempel visar hur man konverterar material till PBR material, och sedan sparar 3D scen i GLTF format:

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
