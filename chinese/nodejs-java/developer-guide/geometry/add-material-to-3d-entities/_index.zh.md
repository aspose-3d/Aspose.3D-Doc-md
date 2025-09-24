---
title: 向 3D 实体添加材质
type: docs
weight: 60
url: "/zh/nodejs-java/add-material-to-3d-entities/"
description: PBR 在游戏引擎视觉效果中起着关键作用，它通过衰减亮度以及散射反射光，实现了光线与表面之间交互的高效且逼真的渲染。开发人员可以使用 Aspose.3D API 将 PBR 材质应用于场景中的 3D 对象。此代码示例演示了如何创建 Box 对象，然后应用 PBR 材质。
---

{{% alert color="primary" %}}

PBR 在游戏引擎视觉效果中起着关键作用，它通过衰减亮度以及散射反射光，实现了光线与表面之间相互作用的高效且逼真的渲染。开发人员可以使用 Aspose.3D API 将 PBR 材料应用于场景中的 3D 对象。此代码示例演示了如何创建 Box 对象，然后应用 PBR 材料。

{{% /alert %}}


## **将 Physically Based Rendering (PBR) 材料应用于 Box**

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// 初始化场景
var scene = new aspose.threed.Scene();

// 初始化 PBR 材料对象
var mat = new aspose.threed.PbrMaterial();

// 几乎是金属的材料
mat.setMetallicFactor(0.9);

// 材料表面非常粗糙
mat.setRoughnessFactor(0.9);

// 创建将应用材料的 Box
var boxNode = scene.getRootNode().createChildNode("box", new aspose.threed.Box());
boxNode.setMaterial(mat);

// 以 USDZ 格式保存 3D 场景
scene.save("PBR_Material_Box_Out.usdz");

{{< /highlight >}}