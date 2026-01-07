---
title: 暴露几何变换
type: docs
weight: 50
url: "/zh/nodejs-java/expose-geometric-transformation/"
description: Aspose.3D for Node.js via Java 允许暴露 3D 场景的几何变换。您可以使用 evaluateGlobalTransform 方法评估全局变换。
---

# **暴露几何变换**
Aspose.3D for Node.js via Java 允许暴露 3D 场景的几何变换。您可以使用 `evaluateGlobalTransform` 方法评估全局变换。以下代码片段展示了如何暴露几何变换。

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// 初始化场景对象
var scene = new aspose.threed.Scene();

// 初始化圆柱体
var cylinder =new aspose.threed.Cylinder();

// 创建 ChildNode
var Node=scene.getRootNode().createChildNode(cylinder);

// 获取几何平移
Node.getTransform().setGeometricTranslation(new aspose.threed.Vector3(10, 0, 0));

// 第一个 Console.WriteLine 将输出包含几何变换的变换矩阵
// 而第二个则不会。
console.log(Node.evaluateGlobalTransform(true));
console.log(Node.evaluateGlobalTransform(false));

{{< /highlight >}}