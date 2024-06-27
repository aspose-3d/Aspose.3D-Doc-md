---
title: Anpassa icke-PBR- konvertering till PBR- material innan du sparar 3D Scener till GLTF 2. 0 Format
type: docs
weight: 70
url: /sv/python-net/customize-non-pbr-to-pbr-materials-conversion-before-saving-3d-scenes-to-gltf-2-0-format/
description: Scenklassen för Aspose.3D API representerar en 3D scen. Utvecklare kan redan bygga en 3D scen genom att lägga till olika enheter. GLTF 2.0 stöder endast PBR-material (Fysiskt baserad rendering), Aspose. 3D API konverterar internt icke-PBR-material till PBR-material innan export till GLTF 2.0.
---
{{% alert color="primary" %}} 

Klassen [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) för Aspose.3D API representerar en 3D scen. Utvecklare kan redan bygga en 3D scen genom att lägga till olika enheter. GLTF 2.0 stöder endast PBR-material (Fysiskt baserad rendering), Aspose. 3D API omvandlar internt icke-PBR-material till PBR-material innan exporten till GLTF 2.0 (materialet i Scenen kommer att förbli oförändrad under exporten), och utvecklarna kan tillhandahålla anpassad konverteringsfunktion för att åsidosätta standardbeteendet.

{{% /alert %}} 
##  **Omvandling av material som inte omfattas av PBR till PBR**
Det här kodexemplet visar hur man konverterar material till PBR-material, och sparar sedan 3D-scenen i GLTF-formatet:

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
