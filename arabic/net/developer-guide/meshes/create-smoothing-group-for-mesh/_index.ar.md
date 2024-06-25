---
title: إنشاء مجموعة تجانس للشبكة
type: docs
weight: 16
url: /ar/net/create-smoothing-group-for-mesh/
description: باستخدام Aspose.3D for .NET ، يمكن للمطورين إنشاء مجموعة تجانس للشبكة.
---
{{% alert color="primary" %}}

باستخدام [Aspose.3D for .NET](https://products.aspose.com/3d/net/) ، يمكن للمطورين إنشاء مجموعة تجانس للشبكة.

{{% /alert %}}

##  **إنشاء مجموعة تجانس للشبكة**
يمكنك إنشاء مثيل `VertexElementSmoothingGroup` بواسطة طريقة `CreateElement` من `Mesh` ، مجموعة التنعيم هي مجموعة من المضلعات في شبكة مضلعة والتي يجب أن تبدو وكأنها تشكل سطحًا سلسًا.


###  **Pروغرامينغ ple وافرة**
هذا المثال رمز يخلق شبكة مكعب ، وإنشاء مجموعة تجانس مثيل مع البيانات المخصصة يدويا.

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

