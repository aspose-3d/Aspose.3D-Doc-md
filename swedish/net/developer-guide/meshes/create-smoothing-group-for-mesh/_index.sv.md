---
title: Skapa utjämnande grupp för mesh
type: docs
weight: 16
url: /sv/net/create-smoothing-group-for-mesh/
description: Med Aspose.3D for .NET kan utvecklare skapa utjämningsgrupp för mesh.
---
{{% alert color="primary" %}}

Med [Aspose.3D for .NET](https://products.aspose.com/3d/net/) kan utvecklare skapa utjämningsgrupp för mesh.

{{% /alert %}}

##  **Skapa utjämnande grupp för mesh**
Du kan skapa en `VertexElementSmoothingGroup` instans med `CreateElement`-metoden för `Mesh`, En utjämnande grupp är en grupp av polygoner i en polygon mesh som bör förefalla bilda en jämn yta.


###  **Programmeringsprova**
Detta kodexempel skapar en kub mesh, och skapa en utjämnande grupp instans med manuellt tilldelade data.

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

