---
title: 创建网格的平滑组
type: docs
weight: 16
url: /zh/net/create-smoothing-group-for-mesh/
description: 使用 Aspose.3D for .NET，开发人员可以为网格创建平滑组。
---
{{% alert color="primary" %}}

使用 [Aspose.3D for .NET](https://products.aspose.com/3d/net/)，开发人员可以为网格创建平滑组。

{{% /alert %}}

##  **创建网格的平滑组**
您可以通过 `Mesh` 的 `CreateElement` 方法创建 `VertexElementSmoothingGroup` 实例，平滑组是多边形网格中的一组多边形，它应该看起来形成平滑曲面。


###  **编程示例**
此代码示例创建一个cube网格，并使用手动指定的数据创建一个平滑组实例。

```
	//create a cube with 6 faces
	var box = (new Box()).ToMesh();
	//create a smoothing group
	var sg = (VertexElementSmoothingGroup)box.CreateElement(VertexElementType.SmoothingGroup, MappingMode.Polygon, ReferenceMode.Direct);
	//assign data for each polygon 
	sg.SetData(new int[] {0, 0, 0, 1, 2, 3 });
	//save the model to FBX file which support VertexElementSmoothingGroup export.
	var scene = new Scene(box);
	scene.Save("box-sg.fbx");
```

