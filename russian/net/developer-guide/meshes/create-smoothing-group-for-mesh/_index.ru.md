---
title: Создание группы сглаживания для сетки
type: docs
weight: 16
url: /ru/net/create-smoothing-group-for-mesh/
description: Используя Aspose.3D for .NET, разработчики могут создавать сглаживающие группы для mesh.
---
{{% alert color="primary" %}}

Используя [Aspose.3D for .NET](https://products.aspose.com/3d/net/), разработчики могут создать группу сглаживания для mesh.

{{% /alert %}}

##  **Создать группу сглаживания для сетки**
Вы можете создать экземпляр `VertexElementSmoothingGroup` методом `CreateElement` из `Mesh`. Группа сглаживания-это группа многоугольников в многоугольной сетке, которая должна образовывать гладкую поверхность.


###  **Образец программирования**
В этом примере кода создается кубическая сетка и создается экземпляр сглаживающей группы с данными, назначенными вручную.

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

