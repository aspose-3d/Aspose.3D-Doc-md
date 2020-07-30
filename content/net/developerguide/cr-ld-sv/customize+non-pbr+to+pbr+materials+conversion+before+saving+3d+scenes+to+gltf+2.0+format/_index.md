---
title : "Customize Non-PBR to PBR Materials Conversion before Saving 3D Scenes to GLTF 2.0 Format" 
description : "" 
weight : 12019 
toc : false
type: docs
url: /net/developerguide/cr-ld-sv/customize+non-pbr+to+pbr+materials+conversion+before+saving+3d+scenes+to+gltf+2.0+format/
---

# Aspose.3D for .NET : Customize Non-PBR to PBR Materials Conversion before Saving 3D Scenes to GLTF 2.0 Format


The [Scene](http://www.aspose.com/api/net/3d/T_Aspose_ThreeD_Scene) class of the Aspose.3D API represents a 3D scene. Developers can already build a 3D scene by adding various entities. GLTF 2.0 only supports PBR (Physically Based Rendering) materials, Aspose.3D API internally converts non-PBR materials into PBR materials before exporting into GLTF 2.0 (the materials in the scene will remain unchanged during the export), and the developers can provide custom convert function to override the default behavior.

## Non-PBR to PBR Material Conversion

This code example demonstrates how to convert material to PBR material, and then saves 3D scene in the GLTF format:

**C#**

{{< code lang="c#" >}}
// initialize a new 3D scene
var s = new Scene();
var box = new Box();
s.RootNode.CreateChildNode("box1", box).Material = new PhongMaterial() {DiffuseColor = new Vector3(1, 0, 1)};
GLTFSaveOptions opt = new GLTFSaveOptions(FileFormat.GLTF2);
//Custom material converter to convert PhongMaterial to PbrMaterial
opt.MaterialConverter = delegate(Material material)
{
    PhongMaterial m = (PhongMaterial) material;
    return new PbrMaterial() {Albedo = new Vector3(m.DiffuseColor.x, m.DiffuseColor.y, m.DiffuseColor.z)};
};
// save in GLTF 2.0 format
s.Save("test.gltf", opt);
{{< /code >}}

