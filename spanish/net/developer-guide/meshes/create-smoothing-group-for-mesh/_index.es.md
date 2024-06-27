---
title: Crear grupo de suavizado para malla
type: docs
weight: 16
url: /es/net/create-smoothing-group-for-mesh/
description: Usando Aspose.3D for .NET, los desarrolladores pueden crear un grupo de suavizado para la malla.
---
{{% alert color="primary" %}}

Con [Aspose.3D for .NET](https://products.aspose.com/3d/net/), los desarrolladores pueden crear un grupo de suavizado para la malla.

{{% /alert %}}

##  **Crear grupo de suavizado para malla**
Puede crear una instancia de `VertexElementSmoothingGroup` mediante el método `CreateElement` de `Mesh`. Un grupo de suavizado es un grupo de polígonos en una malla poligonal que debería aparecer para formar una superficie lisa.


###  **Muestra de programación**
En este ejemplo de código se crea una malla de cubo y se crea una instancia de grupo de suavizado con datos asignados manualmente.

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

