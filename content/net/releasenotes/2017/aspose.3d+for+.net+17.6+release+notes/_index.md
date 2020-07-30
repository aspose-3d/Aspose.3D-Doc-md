---
title : "Aspose.3D for .NET 17.6 Release Notes" 
description : "" 
weight : 12133 
toc : false
type: docs
url: /net/releasenotes/2017/aspose.3d+for+.net+17.6+release+notes/
---

# Aspose.3D for .NET : Aspose.3D for .NET 17.6 Release Notes


This page contains release notes for [Aspose.3D for .NET 17.6](https://www.nuget.org/packages/Aspose.3D/17.6.0).

## Other Improvements and Changes

{{< table style="table-striped" >}}
|Key|Summary|Category|
|:----|:----|:----|
|THREEDNET-257|Export 3D scene into GLTF 2.0 ASCII files|New feature|
|THREEDNET-258|Export 3D scene into GLTF 2.0 Binary files|New feature|
|THREEDNET-264|Models has tangent but has no bi-normal will not render correctly|Bug|
|THREEDNET-267|Materials in Collada files may not be loaded correctly.|Bug|
{{< /table >}}

### Public API and Backwards Incompatible Changes

See the list of any changes made to the public API such as added, renamed, removed or deprecated members as well as any non-backward compatible change made to Aspose.3D for .NET. If you have concerns about any change listed, please raise it on the [Aspose.3D support forum](http://www.aspose.com/community/forums/aspose.3d-product-family/535/showforum.aspx).

#### Adds MaterialConverter Member to Aspose.ThreeD.Formats.GLTFSaveOptions Class

GLTF 2.0 only supports PBR materials, Aspose.3D will internally convert non-PBR materials into PBR materials before exporting into GLTF 2.0 (the materials in the scene will remain unchanged during the export), and the user can provide custom convert function to override the default behavior.

This code example demonstrates how to convert material to PBR material, and then saving 3D scene to GLTF 2.0 format:

**.NET, C#**

{{< code lang="cs" >}}
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
s.Save("test.gltf", opt);
{{< /code >}}

### Usage Examples

Please check the list of help topics added or updated in the Aspose.3D Wiki docs:

1.  [Customize Non-PBR to PBR Materials Conversion before Saving 3D Scenes to GLTF 2.0 Format ](https://docs2.aspose.com/3d/net/developerguide/cr-ld-sv/customize+non-pbr+to+pbr+materials+conversion+before+saving+3d+scenes+to+gltf+2.0+format)

