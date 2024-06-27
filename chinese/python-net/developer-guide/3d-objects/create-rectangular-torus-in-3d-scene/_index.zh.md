---
title: 在 3D 场景中创建矩形圆环
type: docs
weight: 50
url: /zh/python-net/create-rectangular-torus-in-3d-scene/
description: 使用 Aspose.3D for Python via .NET API，开发人员可以创建 3D 对象，然后以任何受支持的 3D 格式保存 3D 场景。
---
{{% alert color="primary" %}} 

使用 [Aspose.3D for Python via .NET](https://products.aspose.com/3d/python-net/) API，开发人员可以创建 3D 对象，然后以任何受支持的 3D 格式保存 3D 场景。

{{% /alert %}} 
##  **矩形圆环**
我们添加了 `RectangularTorus` 类，它允许开发人员将参数化的矩形圆环放入场景中，这可以在将场景保存为不同的支持文件格式时转换为有序网格/三角形网格。

**Python**

```py

import math
from aspose.threed.entities import RectangularTorus

rt = RectangularTorus()

rt.inner_radius = 17

rt.outer_radius = 22

rt.height = 30

rt.arc = math.pi * 0.5

scene = Scene()

scene.root_node.create_child_node(rt)

scene.save("rtorus.obj", FileFormat.WAVEFRONT_OBJ)

```

生成的矩形圆环如下所示:

![todo: 图像 _ alt_text](create-rectangular-torus-in-3d-scene_1.png)
