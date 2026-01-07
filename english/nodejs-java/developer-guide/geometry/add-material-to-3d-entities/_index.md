---
title: Add Material to 3D Entities
type: docs
weight: 60
url: /nodejs-java/add-material-to-3d-entities/
description: PBR plays a key role for the game engine visuals, with its efficient and realistic rendering of interactions between light and surface via attenuation of the brightness and scattering of reflected light. Developers can use Aspose.3D API to apply PBR material to 3D objects in a scene. This code example demonstrates to how to create a Box object, and then apply the PBR material.
---

{{% alert color="primary" %}}

PBR plays a key role for the game engine visuals, with its efficient and realistic rendering of interactions between light and surface via attenuation of the brightness and scattering of reflected light. Developers can use Aspose.3D API to apply PBR material to 3D objects in a scene. This code example demonstrates to how to create a Box object, and then apply the PBR material.

{{% /alert %}}


## **Apply Physically Based Rendering (PBR) Material to a Box**

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// initialize a scene
var scene = new aspose.threed.Scene();

// initialize PBR material object
var mat = new aspose.threed.PbrMaterial();

// an almost metal material
mat.setMetallicFactor(0.9);

// material surface is very rough
mat.setRoughnessFactor(0.9);

// create a box to which the material will be applied
var boxNode = scene.getRootNode().createChildNode("box", new aspose.threed.Box());
boxNode.setMaterial(mat);

// save 3d scene into USDZ format
scene.save("PBR_Material_Box_Out.usdz");

{{< /highlight >}}
