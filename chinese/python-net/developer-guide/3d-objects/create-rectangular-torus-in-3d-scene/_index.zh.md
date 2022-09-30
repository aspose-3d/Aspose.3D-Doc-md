---
title: 在3D场景中创建矩形圆环
type: docs
weight: 50
url: /zh/python-net/create-rectangular-torus-in-3d-scene/
description: 使用Aspose.3D进行Python via .NET API，开发人员可以创建3D对象，然后以任何支持的3D格式保存3D场景。
---
{{% alert color="primary" %}} 

使用[Aspose.3D为Python via .NET](https://products.aspose.com/3d/python-net/)API，开发人员可以创建3D对象，然后以任何支持的3D格式保存3D场景。

{{% /alert %}} 
## **矩形圆环**
我们添加了`RectangularTorus`类，它允许开发人员将参数化的矩形圆环放入场景中，这可以在将场景保存为不同支持的文件格式期间转换为序数网格/三角形网格。

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

![todo: 图像_alt_文本](create-rectangular-torus-in-3d-scene_1.png)
