---
title: 创建带有基本 3D 形状的场景
type: docs
weight: 20
url: "/zh/nodejs-java/create-scene-with-primitive-3d-shapes/"
description: Aspose.3D for Node.js 通过 Java API 具有对基本 3D 形状的支持。所有参数化基本体在保存到任何受支持的输出文件格式时，都将自动转换为网格。
---

{{% alert color="primary" %}} 

Aspose.3D for Node.js via Java API has support of primitive 3D shapes. All parameterized primitives will be converted to mesh automatically while saving in any supported output file format.

{{% /alert %}} 
## **Build Scene from Primitive 3D Shapes**
Modeling is the process of pure creation and Aspose.3D API supports creating a scene with primitive 3D shapes.
### **Programming Sample**
This code example creates a scene with primitive 3D shapes and save in the OBJ file.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Initialize a 3D scene
var scene = new aspose.threed.Scene();

// Create a Box model
scene.getRootNode().createChildNode("box", new aspose.threed.Box());

// Create a Cylinder model
scene.getRootNode().createChildNode("cylinder", new aspose.threed.Cylinder());

// Save drawing in the OBJ format
scene.save("test.obj");


{{< /highlight >}}