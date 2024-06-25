---
title: 创建一个空的 3D 文档
type: docs
weight: 20
url: /zh/nodejs-java/create-an-empty-3d-document/
description: Aspose.3D for Node.js via Java API 支持从头开始创建 3D 场景，然后以支持的 3D 格式保存。
---
##  **创建一个空的 3D 场景并以支持的 3D 格式保存**
Aspose.3D for Node.js via Java API 支持从头开始创建 3D 场景，然后以支持的 3D 格式保存。
###  **创建空 3D 场景**
请按照以下步骤创建包含 Aspose.3D for Node.js via Java API 的 3D 场景:

1. 创建一个实例**场景**表示 3D 场景的类。
1. 通过调用生成 3D 文档**保存**的方法**场景**类实例。
####  **创建空 3D 场景: 编程示例**
{{< highlight "java" >}}

var file="document.fbx";

// Create an object of the Scene class
var scene = new aspose.threed.Scene();

// Save 3D scene document
scene.save(file);

{{< /highlight >}}




