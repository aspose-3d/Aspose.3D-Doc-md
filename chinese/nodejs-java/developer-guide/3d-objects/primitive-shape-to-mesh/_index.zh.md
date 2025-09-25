---
title: 将基本形状转换为网格
type: docs
weight: 20
url: "/zh/nodejs-java/primitive-shape-to-mesh/"
description: Aspose.3D for Node.js 通过 Java API 支持将任何基本形状转换为网格。基本形状包括大多数基本和常用的对象，例如盒子、球体、平面、圆柱体和甜甜圈。
---

## **将基本形状转换为网格**
Aspose.3D for Node.js 通过 Java API 支持将任何基本形状转换为网格。基本形状包括大多数基本和常用的对象，例如盒子、球体、平面、圆柱体和甜甜圈。

{{% alert color="primary" %}}

可以转换为网格并在导出到任何 3D 文件格式时，实现 IMeshConvertible 接口的任何类都可以转换成网格。

{{% /alert %}}
### **将球体基本形状转换为网格**
球体是三维空间中完美的圆形几何物体，从运动球到太空中的行星无处不在。让我们使用球体基本形状来创建网格。
下面的代码示例将球体转换为网格。

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// 使用 Sphere 类初始化对象
var convertible = new aspose.threed.Sphere();

// 将球体转换为网格
var mesh = convertible.toMesh();

{{< /highlight >}}

### **将盒子转换为网格**
盒子描述了各种用于永久存储或临时使用的容器，通常用于运输内容。让我们使用盒子基本形状来创建网格。下面的代码示例将盒子转换为网格。

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// 使用 Box 类初始化对象
var convertible = new aspose.threed.Box();

// 将盒子转换为网格
var mesh = convertible.toMesh();

{{< /highlight >}}

### **将平面转换为网格**
平面在三维空间中无限延伸，没有厚度。平面的一个例子是坐标平面。让我们使用平面基本形状来创建网格。下面的代码示例将平面转换为网格。

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// 使用 Plane 类初始化对象
var convertible = new aspose.threed.Plane();

// 将平面转换为网格
var mesh = convertible.toMesh();

{{< /highlight >}}

### **将圆柱体转换为网格**
圆柱体是最基本的曲线几何形状之一，它是从给定直线（圆柱体的轴）保持固定距离的点组成的曲面。它可以在许多地方使用，例如房屋前方的柱子或汽车传动轴。让我们使用圆柱体基本形状来创建网格。下面的代码示例将圆柱体转换为网格。

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// 使用 Cylinder 类初始化对象
var convertible = new aspose.threed.Cylinder();

// 将圆柱体转换为网格
var mesh = convertible.toMesh();

{{< /highlight >}}

### **将甜甜圈转换为网格**
甜甜圈是三维空间中通过将圆绕平面上的轴旋转而生成的曲面。如果旋转轴不接触圆，则该曲面具有环形形状，称为旋转甜甜圈。让我们使用甜甜圈基本形状来创建网格。下面的代码示例将甜甜圈转换为网格。

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// 使用 Torus 类初始化对象
var convertible = new aspose.threed.Torus();

// 将甜甜圈转换为网格
var mesh = convertible.toMesh();

{{< /highlight >}}