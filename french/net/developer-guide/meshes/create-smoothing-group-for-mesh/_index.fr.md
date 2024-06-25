---
title: Créer un groupe de lissage pour le maillage
type: docs
weight: 16
url: /fr/net/create-smoothing-group-for-mesh/
description: En utilisant Aspose.3D for .NET, les développeurs peuvent créer un groupe de lissage pour le maillage.
---
{{% alert color="primary" %}}

En utilisant [Aspose.3D for .NET](https://products.aspose.com/3d/net/), les développeurs peuvent créer un groupe de lissage pour le maillage.

{{% /alert %}}

##  **Créer un groupe de lissage pour le maillage**
Vous pouvez créer une instance `VertexElementSmoothingGroup` par la méthode `CreateElement` de `Mesh`, un groupe de lissage est un groupe de polygones dans un maillage de polygone qui devrait apparaître pour former une surface lisse.


###  **Échantillon de programmation**
Cet exemple de code crée un maillage cube et crée une instance de groupe de lissage avec des données affectées manuellement.

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

