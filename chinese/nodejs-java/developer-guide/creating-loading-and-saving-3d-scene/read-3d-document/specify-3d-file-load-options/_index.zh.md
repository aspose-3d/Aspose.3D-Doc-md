---
title: 指定 3D 文件加载选项
type: docs
weight: 10
url: "/zh/nodejs-java/specify-3d-file-load-options/"
description: 有几个 Scene.open 方法重载或 Scene 类构造函数重载接受 LoadOptions 实例。
---

## **3D 文件加载选项**
有几种 `Scene.open` 方法重载或 `Scene` 类构造函数重载接受 `LoadOptions` 实例。这应该是一个派生自 `LoadOptions` 类的类的实例。每种加载格式都有一个对应的类来持有该加载格式的选项，例如，对于 `FileFormat.COLLADA` 保存格式，有 `ColladaSaveOptions`。
### **使用 Discreet 3DS 加载选项**
下面的代码展示了如何在加载 Discreet 3DS 文件之前设置加载选项。

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

var loadOpts = new aspose.threed.Discreet3dsLoadOptions();

// 设置是否使用动画轨迹中的第一帧定义的变换。
loadOpts.setApplyAnimationTransform(true);

// 翻转坐标系
loadOpts.setFlipCoordinateSystem(true);

// 优先使用 gamma 校正颜色，如果 3ds 文件同时提供原始颜色和 gamma 校正颜色。
loadOpts.setGammaCorrectedColor(true);

{{< /highlight >}}

### **使用 Obj 加载选项**
下面的代码展示了如何在加载 3D Obj 文件之前设置加载选项。

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

var loadObjOpts  = new aspose.threed.ObjLoadOptions();

// 从外部材质库文件导入材质
loadObjOpts.setEnableMaterials(true);

// 翻转坐标系。
loadObjOpts.setFlipCoordinateSystem(true);

{{< /highlight >}}

### **使用 STL 加载选项**
下面的代码展示了如何在加载 STL 文件之前设置加载选项。

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// 初始化一个对象
var loadSTLOpts   = new aspose.threed.StlLoadOptions();

// 翻转坐标系。
loadSTLOpts.setFlipCoordinateSystem(true);

{{< /highlight >}}

### **使用 U3D 加载选项**
下面的代码展示了如何在加载 U3D 文件之前设置加载选项。

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// 初始化一个对象
var loadU3DOpts = new aspose.threed.U3dLoadOptions();

// 翻转坐标系。
loadU3DOpts.setFlipCoordinateSystem(true);

{{< /highlight >}}

### **使用 glTF 加载选项**
下面的代码展示了如何在加载 glTF 文件之前设置加载选项。

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// 设置加载选项
var loadOpt = new aspose.threed.GltfLoadOptions();

// 默认值为 true，通常我们不需要更改它。 Aspose.3D 会在加载和保存期间自动翻转 V/T 纹理坐标。
loadOpt.setFlipTexCoordV(true);

{{< /highlight >}}

### **使用 Ply 加载选项**
下面的代码展示了如何在加载 PLY 模型之前设置加载选项。

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// 初始化 Scene 类对象
var scene = new aspose.threed.Scene();

// 初始化一个对象
var loadPLYOpts  = new aspose.threed.PlyLoadOptions();

// 翻转坐标系。
loadPLYOpts.setFlipCoordinateSystem(true);

// 加载 3D Ply 模型
scene.open("vase-v2.ply", loadPLYOpts);

{{< /highlight >}}

### **使用 DirectX X 加载选项**
下面的代码展示了如何在加载 DirectX X 文件之前设置加载选项。

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// 初始化 Scene 类对象
var scene = new aspose.threed.Scene();

// 初始化一个对象
var loadXOpts = new aspose.threed.XLoadOptions(aspose.threed.FileContentType.ASCII);

// 翻转坐标系。
loadXOpts.setFlipCoordinateSystem(true);

// 加载 3D X 文件
scene.open("warrior.x", loadXOpts);

{{< /highlight >}}

### **使用 FBX 加载选项**

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// 这将输出 FBX 文件中 GlobalSettings 中定义的全部属性。
var opt = new aspose.threed.FbxLoadOptions();

opt.setKeepBuiltinGlobalSettings(true);

{{< /highlight >}}