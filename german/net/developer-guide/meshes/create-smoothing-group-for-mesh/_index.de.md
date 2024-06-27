---
title: Glättung gruppe für Mesh erstellen
type: docs
weight: 16
url: /de/net/create-smoothing-group-for-mesh/
description: Mit Aspose.3D for .NET können Entwickler eine Glättung gruppe für Mesh erstellen.
---
{{% alert color="primary" %}}

Mit [Aspose.3D for .NET](https://products.aspose.com/3d/net/) können Entwickler eine Glättung gruppe für Mesh erstellen.

{{% /alert %}}

##  **Glättung gruppe für Mesh erstellen**
Sie können eine `VertexElementSmoothingGroup`-Instanz mit der `CreateElement`-Methode von `Mesh` erstellen. Eine Glättung gruppe ist eine Gruppe von Polygonen in einem Polygon netz, die eine glatte Oberfläche bilden sollten.


###  **Programmier probe**
In diesem Code beispiel wird ein Cube-Mesh erstellt und eine Glättung gruppen instanz mit manuell zugewiesenen Daten erstellt.

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

