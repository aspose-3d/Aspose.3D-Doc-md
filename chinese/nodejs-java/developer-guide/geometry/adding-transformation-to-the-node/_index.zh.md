---
title: 向节点添加转换
type: docs
weight: 10
url: "/zh/nodejs-java/adding-transformation-to-the-node/"
description: "Aspose.3D for Node.js 通过 Java API 具有支持在 3D 空间中旋转对象的功能。有三种定义对象在 3D 空间中旋转的方式，欧拉角、四元数和自定义矩阵，它们都由 Transform 类支持。"
---

{{% alert color="primary" %}}

Aspose.3D for Node.js via Java API 具有支持在 3D 空间中旋转对象的功能。有三种定义对象在 3D 空间中旋转的方式，欧拉角、四元数和自定义矩阵，它们都由 `Transform` 类支持。

{{% /alert %}}

TSR（平移/缩放/旋转）在 3D 场景中最常用，我们提供了 `Transform` 类来访问这些功能，Aspose.3D 仿射变换包括：

- 平移
- 缩放
- 旋转
- 剪切映射
- 挤压映射

## **通过欧拉角旋转**

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// 初始化场景对象
var scene = new aspose.threed.Scene();

// 初始化圆柱体
var cylinder =new aspose.threed.Cylinder(2, 2, 10, 20, 1, false);

// 创建 ChildNode
var Node=scene.getRootNode().createChildNode(cylinder);

// 欧拉角
Node.getTransform().setEulerAngles(new aspose.threed.Vector3(30, 40, 50));

// 设置平移
Node.getTransform().setTranslation(new aspose.threed.Vector3(0, 0, 20));

// 保存
scene.save("TransformationToNode.obj");

{{< /highlight >}}

## **自定义变换矩阵**
我们也可以直接使用矩阵：

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// 初始化场景对象
var scene = new aspose.threed.Scene();

// 初始化圆柱体
var cylinder =new aspose.threed.Cylinder(2, 2, 10, 20, 1, false);

// 创建 ChildNode
var Node=scene.getRootNode().createChildNode(cylinder);

// 设置自定义平移矩阵
Node.getTransform().setTransformMatrix(new aspose.threed.Matrix4(
    1, -0.3, 0, 0,
    0.4, 1, 0.3, 0,
    0, 0, 1, 0,
    0, 20, 0, 1
));

// 保存
scene.save("TransformationToNode.obj");

{{< /highlight >}}
