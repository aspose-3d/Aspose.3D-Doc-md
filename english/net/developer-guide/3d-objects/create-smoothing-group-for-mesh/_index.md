---
title: Create smoothing group for mesh
type: docs
weight: 70
url: /net/create-smoothing-group-for-mesh/
description: Using Aspose.3D for .NET, developers can create smoothing group for mesh.
---

{{% alert color="primary" %}}

Using [Aspose.3D for .NET](https://products.aspose.com/3d/net/), developers can create smoothing group for mesh.

{{% /alert %}}

## **Create Smoothing group for mesh**
You can create a `VertexElementSmoothingGroup` instance by `CreateElement` method of `Mesh`, A smoothing group is a group of polygons in a polygon mesh which should appear to form a smooth surface.


### **Programming Sample**
This code example creates a cube mesh, and create a smoothing group instance with manually assigned data.

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

