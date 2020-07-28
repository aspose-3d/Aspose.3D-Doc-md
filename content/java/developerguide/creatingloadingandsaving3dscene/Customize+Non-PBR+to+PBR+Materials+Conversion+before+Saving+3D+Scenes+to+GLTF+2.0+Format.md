+++
title = "Customize Non-PBR to PBR Materials Conversion before Saving 3D Scenes to GLTF 2.0 Format" 
description = "" 
weight = 12018 
+++

Aspose.3D for Java : Customize Non-PBR to PBR Materials Conversion before Saving 3D Scenes to GLTF 2.0 Format  

# Aspose.3D for Java : Customize Non-PBR to PBR Materials Conversion before Saving 3D Scenes to GLTF 2.0 Format


The **Scene** class of the Aspose.3D for Java API represents a 3D scene and developers can build a 3D scene by adding various entities. GLTF 2.0 only supports PBR (Physically Based Rendering) materials, Aspose.3D API internally converts non-PBR materials into PBR materials before exporting into GLTF 2.0 (the materials in the scene will remain unchanged during the export), and the developers can provide custom convert function to override the default behavior.

## Non-PBR to PBR Material Conversion

This code example demonstrates how to convert material to PBR material, and then saves 3D scene in the GLTF format:

