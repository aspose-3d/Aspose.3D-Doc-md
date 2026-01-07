---
title: 线性挤出加工
type: docs
weight: 80
url: "/zh/nodejs-java/working-with-linear-extrusion/"
description: Aspose.3D for Node.js via Java 提供了 LinearExtrusion 类，该类接受一个 2D 形状作为输入，并在 3 维空间中扩展该形状。
---

# **Performing Linear Extrusion**
Aspose.3D for Node.js via Java 提供了 `LinearExtrusion` 类，它将 2D 形状作为输入并将其延伸到 3 维空间中。以下代码片段展示了如何执行线性挤压：

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// 初始化要挤压的基础形状
// 初始化要挤压的基础轮廓
var profile=new aspose.threed.RectangleShape();
profile.setRoundingRadius(0.3);

// 通过传递 2D 形状作为输入并将其延伸到 3 维空间中执行线性挤压
var extrusion =new aspose.threed.LinearExtrusion(profile, 10);
extrusion.setSlices(100);
extrusion.setCenter(true);
extrusion.setTwist(360);
extrusion.setTwistOffset(new aspose.threed.Vector3(10, 0, 0));

// 创建场景
var scene = new aspose.threed.Scene();

// 通过传递挤压创建子节点
scene.getRootNode().createChildNode(extrusion);

// 保存 3D 场景
scene.save("LinearExtrusion.obj");

{{< /highlight >}}

# **Slices in Linear Extrusion**
Aspose.3D for Node.js via Java 提供了 `setSlices()` 方法的 `LinearExtrusion` 类。 `setSlices()` 方法定义了挤压路径上的中间点数。 以下代码片段展示了如何在线性挤压中使用 `setSlices()` 方法：

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// 初始化要挤压的基础轮廓
var profile=new aspose.threed.RectangleShape();
profile.setRoundingRadius(0.3);

// 创建场景
var scene = new aspose.threed.Scene();

// 创建左侧节点
var left=scene.getRootNode().createChildNode();
// 创建右侧节点
var right=scene.getRootNode().createChildNode();
left.getTransform().setTranslation(new aspose.threed.Vector3(5, 0, 0));

// Slices 参数定义了挤压路径上的中间点数
// 使用 slices 属性在左侧节点上执行线性挤压
var extrusion1 =new aspose.threed.LinearExtrusion(profile, 2);
extrusion1.setSlices(2);
left.createChildNode(extrusion1);

// 使用 slices 属性在右侧节点上执行线性挤压
var extrusion2 =new aspose.threed.LinearExtrusion(profile, 2);
extrusion2.setSlices(10);
right.createChildNode(extrusion2);

// 保存 3D 场景
scene.save("SlicesInLinearExtrusion.obj");

{{< /highlight >}}

# **Center in Linear Extrusion**
Aspose.3D for Node.js via Java 提供了 `setCenter()` 方法的 `LinearExtrusion` 类。 如果将 `setCenter()` 方法设置为 true，则挤压范围为 -Height/2 到 Height/2，否则，挤压范围为 0 到 Height。 以下代码片段展示了如何在线性挤压中使用 `setCenter()` 方法：

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// 初始化要挤压的基础轮廓
var profile=new aspose.threed.RectangleShape();
profile.setRoundingRadius(0.3);

// 创建场景
var scene = new aspose.threed.Scene();

// 创建左侧节点
var left=scene.getRootNode().createChildNode();
// 创建右侧节点
var right=scene.getRootNode().createChildNode();
left.getTransform().setTranslation(new aspose.threed.Vector3(5, 0, 0));

// 为了参考设置地面平面
var box=new aspose.threed.Box(0.01, 3, 3);

// 如果 Center 属性为 true，则挤压范围为 -Height/2 到 Height/2，否则挤压范围为 0 到 Height
// 使用 center 和 slices 属性在左侧节点上执行线性挤压
var extrusion1 =new aspose.threed.LinearExtrusion(profile, 2);
extrusion1.setSlices(3);
extrusion1.setCenter(false);
left.createChildNode(extrusion1);
left.createChildNode(box);

// 使用 center 和 slices 属性在右侧节点上执行线性挤压
var extrusion2 =new aspose.threed.LinearExtrusion(profile, 2);
extrusion2.setSlices(3);
extrusion2.setCenter(true);
right.createChildNode(extrusion2);
right.createChildNode(box);

// 保存 3D 场景
scene.save("CenterInLinearExtrusion.obj");

{{< /highlight >}}

# **Twist in Linear Extrusion**
Aspose.3D for Node.js via Java 提供了 `setTwist()` 方法的 `LinearExtrusion` 类。 `setTwist()` 方法处理在挤压形状时旋转的度数。 以下代码片段展示了如何在线性挤压中使用 `setTwist()` 方法：

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// 初始化要挤压的基础轮廓
var profile=new aspose.threed.RectangleShape();
profile.setRoundingRadius(0.3);

// 创建场景
var scene = new aspose.threed.Scene();

// 创建左侧节点
var left=scene.getRootNode().createChildNode();
// 创建右侧节点
var right=scene.getRootNode().createChildNode();
left.getTransform().setTranslation(new aspose.threed.Vector3(5, 0, 0));

// Twist 属性定义了在挤压轮廓时旋转的度数
// 使用 twist 和 slices 属性在左侧节点上执行线性挤压
var extrusion1 =new aspose.threed.LinearExtrusion(profile, 10);
extrusion1.setSlices(100);
extrusion1.setTwist(360);
left.createChildNode(extrusion1);

// 使用 twist、twist offset 和 slices 属性在右侧节点上执行线性挤压
var extrusion2 =new aspose.threed.LinearExtrusion(profile, 10);
extrusion2.setSlices(100);
extrusion2.setTwist(360);
extrusion2.setTwistOffset(new aspose.threed.Vector3(3, 0, 0));
right.createChildNode(extrusion2);

// 保存 3D 场景
scene.save("TwistOffsetInLinearExtrusion.obj");

{{< /highlight >}}

# **Twist Offset in Linear Extrusion**
Aspose.3D for Node.js via Java 提供了 `setTwistOffset()` 方法的 `LinearExtrusion` 类。 `setTwistOffset()` 方法定义了挤压形状时旋转的偏移量。 以下代码片段展示了如何在线性挤压中使用 `setTwistOffset()` 方法：

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// 初始化要挤压的基础轮廓
var profile=new aspose.threed.RectangleShape();
profile.setRoundingRadius(0.3);

// 创建场景
var scene = new aspose.threed.Scene();

// 创建左侧节点
var left=scene.getRootNode().createChildNode();
// 创建右侧节点
var right=scene.getRootNode().createChildNode();
left.getTransform().setTranslation(new aspose.threed.Vector3(5, 0, 0));

// Twist 属性定义了在挤压轮廓时旋转的度数
// 使用 twist 和 slices 属性在左侧节点上执行线性挤压
var extrusion1 =new aspose.threed.LinearExtrusion(profile, 10);
extrusion1.setSlices(100);
extrusion1.setTwist(360);
left.createChildNode(extrusion1);

// 使用 twist、twist offset 和 slices 属性在右侧节点上执行线性挤压
var extrusion2 =new aspose.threed.LinearExtrusion(profile, 10);
extrusion2.setSlices(100);
extrusion2.setTwist(360);
extrusion2.setTwistOffset(new aspose.threed.Vector3(3, 0, 0));
right.createChildNode(extrusion2);

// 保存 3D 场景
scene.save("TwistOffsetInLinearExtrusion.obj");

{{< /highlight >}}

# **Direction in Linear Extrusion**
Aspose.3D for Node.js via Java 提供了 `setDirection()` 方法的 `LinearExtrusion` 类。 `setDirection()` 方法定义了挤压的方向。 以下代码片段展示了如何在线性挤压中使用 `setDirection()` 方法：

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// 初始化要挤压的基础轮廓
var profile=new aspose.threed.RectangleShape();
profile.setRoundingRadius(0.3);

// 创建场景
var scene = new aspose.threed.Scene();

// 创建左侧节点
var left=scene.getRootNode().createChildNode();
// 创建右侧节点
var right=scene.getRootNode().createChildNode();
left.getTransform().setTranslation(new aspose.threed.Vector3(5, 0, 0));

// Direction 属性定义了挤压的方向。
// 使用 twist 和 slices 属性在左侧节点上执行线性挤压
var extrusion1 =new aspose.threed.LinearExtrusion(profile, 10);
extrusion1.setSlices(100);
extrusion1.setTwist(360);
left.createChildNode(extrusion1);

// 使用 twist、slices 和 direction 属性在右侧节点上执行线性挤压
var extrusion2 =new aspose.threed.LinearExtrusion(profile, 10);
extrusion2.setSlices(100);
extrusion2.setTwist(360);
extrusion2.setDirection(new aspose.threed.Vector3(0.3, 0.2, 1));
right.createChildNode(extrusion2);

// 保存 3D 场景
scene.save("DirectionInLinearExtrusion.obj");

{{< /highlight >}}
