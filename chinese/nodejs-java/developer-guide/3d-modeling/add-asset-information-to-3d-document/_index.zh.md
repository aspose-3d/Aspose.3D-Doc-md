---
title: 向 3D 文档添加资产信息
type: docs
weight: 10
url: "/zh/nodejs-java/add-asset-information-to-3d-document/"
description: 元数据是描述、解释、定位信息资源，或使其更容易检索、使用或管理的结构化信息。Aspose.3D for Node.js via Java API 支持定义场景的元数据。
---

## **向 3D 文档添加资产信息**
元数据是描述、解释、定位或使其更容易检索、使用或管理信息资源的结构化信息。Aspose.3D for Node.js via Java API 支持为场景定义元数据。
### **为场景定义元数据**
3D 节目会产生大量的元数据和图像信息。元数据是资产和节目的组成部分。

1. 使用 `Scene` 类初始化 3D 场景。
1. 设置应用程序/工具名称。
1. 设置应用程序/工具供应商名称。
1. 设置测量单位。
1. 设置测量单位比例因子。
1. 以受支持的文件格式保存 3D 场景。

在此示例中，我们假设场景是由名为“Egypt”的 CAD 工具创建的，并且由“Manualdesk”设计：

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// 初始化 3D 场景
var scene = new aspose.threed.Scene();

// 初始化 Box 对象
var box=new aspose.threed.Box();

// 将 Box 对象添加到场景
scene.getRootNode().createChildNode(box);

// 设置应用程序/工具名称
scene.getAssetInfo().setApplicationName("Egypt");

// 设置应用程序/工具供应商名称
scene.getAssetInfo().setApplicationVendor("Manualdesk");

// 我们使用古埃及的测量单位 Pole
scene.getAssetInfo().setUnitName("pole");

// 一 Pole 等于 60 厘米
scene.getAssetInfo().setUnitScaleFactor(0.6);

scene.save("InformationToScene.obj");

{{< /highlight >}}