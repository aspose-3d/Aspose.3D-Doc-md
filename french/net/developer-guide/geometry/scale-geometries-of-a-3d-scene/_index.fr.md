---
title: Géométries d'échelle d'une scène 3D
type: docs
weight: 70
url: /fr/net/scale-geometries-of-a-3d-scene/
description: Les développeurs ne peuvent mettre à l'échelle que les géométries d'un nœud 3D ou de tous les nœuds de 3D Scene. Pour ce faire, les développeurs peuvent appeler plusieurs membres Scale de l'instance de classe PolygonModifier.
---
## **Géométries d'échelle d'un seul nœud 3D ou de tous les nœuds de 3D Scène**
Les développeurs ne peuvent mettre à l'échelle que les géométries d'un nœud 3D ou de tous les nœuds de 3D Scene. Pour ce faire, les développeurs peuvent appeler plusieurs membres Scale de l'instance de classe `PolygonModifier`. C'est l'exemple de code pour mettre à l'échelle tous les nœuds ou un seul nœud:



**C#**

{{< highlight "java" >}}

 // scale the model in huge-scene.obj by 0.01 and save it to another file:

Scene scene = new Scene("huge-scene.obj");

// create a Box instance

var box = scene.RootNode.CreateChildNode("box", new Box());

// scale geometries of a single node

PolygonModifier.Scale(box, new Vector3(0.01));

// scale geometries of all nodes

PolygonModifier.Scale(scene, new Vector3(0.01));

scene.Save("scaled-scene.obj", FileFormat.WavefrontOBJ);

{{< /highlight >}}
