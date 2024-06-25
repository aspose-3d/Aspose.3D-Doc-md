---
title: Anpassa icke-PBR- konvertering till PBR- material innan du sparar 3D Scener till GLTF 2. 0 Format
type: docs
weight: 50
url: /sv/java/customize-non-pbr-to-pbr-materials-conversion-before-saving-3d-scenes-to-gltf-2-0-format/
description: Scenklassen för Aspose. 3D for Java API representerar en 3D scen och utvecklare kan bygga en 3D scen genom att lägga till. Olika enheter.
---
{{% alert color="primary" %}} 

The `Scene` class of the Aspose.3D for Java API represents a 3D scene and developers can build a 3D scene by adding various entities. GLTF 2.0 only supports PBR (Physically Based Rendering) materials, Aspose.3D API internally converts non-PBR materials into PBR materials before exporting into GLTF 2.0 (the materials in the scene will remain unchanged during the export), and the developers can provide custom convert function to override the default behavior.

{{% /alert %}} 
##  **Omvandling av material som inte omfattas av PBR till PBR**
Det här kodexemplet visar hur man konverterar material till PBR-material, och sparar sedan 3D-scenen i GLTF-formatet:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-Non_PBRtoPBRMaterial.java" >}}
