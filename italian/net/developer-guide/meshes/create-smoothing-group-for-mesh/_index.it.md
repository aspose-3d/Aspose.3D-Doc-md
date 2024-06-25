---
title: Crea un gruppo di levigatura per la mesh
type: docs
weight: 16
url: /it/net/create-smoothing-group-for-mesh/
description: Utilizzando Aspose.3D for .NET, gli sviluppatori possono creare un gruppo di smoothing per la mesh.
---
{{% alert color="primary" %}}

Utilizzando [Aspose.3D for .NET](https://products.aspose.com/3d/net/), gli sviluppatori possono creare un gruppo di smoothing per la mesh.

{{% /alert %}}

##  **Crea gruppo Smoothing per mesh**
Puoi creare un'istanza `VertexElementSmoothingGroup` con il metodo `CreateElement` di `Mesh`, un gruppo di smoothing è un gruppo di poligoni in una mesh poligonale che dovrebbe sembrare formare una superficie liscia.


###  **Campione di programmazione**
Questo esempio di codice crea una mesh cubica e crea un'istanza di gruppo di smussamento con dati assegnati manualmente.

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

