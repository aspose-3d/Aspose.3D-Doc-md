---
title: Customize Non-PBR to PBR Materials Conversion before Saving 3D Scenes to GLTF 2.0 Format
type: docs
weight: 50
url: /java/customize-non-pbr-to-pbr-materials-conversion-before-saving-3d-scenes-to-gltf-2-0-format/
---

{{% alert color="primary" %}} 

The **Scene** class of the Aspose.3D for Java API represents a 3D scene and developers can build a 3D scene by adding various entities. GLTF 2.0 only supports PBR (Physically Based Rendering) materials, Aspose.3D API internally converts non-PBR materials into PBR materials before exporting into GLTF 2.0 (the materials in the scene will remain unchanged during the export), and the developers can provide custom convert function to override the default behavior.

{{% /alert %}} 
## **Non-PBR to PBR Material Conversion**
This code example demonstrates how to convert material to PBR material, and then saves 3D scene in the GLTF format:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-Non_PBRtoPBRMaterial.java" >}}
