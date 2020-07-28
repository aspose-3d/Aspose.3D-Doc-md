+++
title = "Scale geometries of a 3D Scene" 
description = "" 
weight = 12029 
+++

Aspose.3D for .NET : Scale geometries of a 3D Scene  

# Aspose.3D for .NET : Scale geometries of a 3D Scene


{{< panel title="Contents Summary" style="primary" >}}
*   1 [Scale geometries of a single 3D node or all nodes of 3D Scene](#Scalegeometriesofa3DScene-Scalegeometriesofasingle3Dnodeorallnodesof3DScene)
{{< /panel >}}
 

 

## Scale geometries of a single 3D node or all nodes of 3D Scene

Developers can scale only geometries of a 3D node or all nodes of 3D Scene. In order to achieve this, developers can call multiple Scale members of the PolygonModifier class instance. This is the code example to scale all nodes or single node:

**C#**

{{< code lang="c#" >}}
// scale the model in huge-scene.obj by 0.01 and save it to another file:
Scene scene = new Scene("huge-scene.obj");
// create a Box instance
var box = scene.RootNode.CreateChildNode("box", new Box());
// scale geometries of a single node
PolygonModifier.Scale(box, new Vector3(0.01));
// scale geometries of all nodes
PolygonModifier.Scale(scene, new Vector3(0.01));
scene.Save("scaled-scene.obj", FileFormat.WavefrontOBJ);
{{< /code >}}

