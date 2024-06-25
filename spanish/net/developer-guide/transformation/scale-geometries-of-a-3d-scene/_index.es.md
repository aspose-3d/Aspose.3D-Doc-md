---
title: Geometrías de escala de una escena 3D
type: docs
weight: 70
url: /es/net/scale-geometries-of-a-3d-scene/
description: Los desarrolladores pueden escalar solo las geometrías de un nodo 3D o todos los nodos de 3D Scene. Para lograr esto, los desarrolladores pueden llamar a varios miembros de Scale de la instancia de la clase PolygonModifier.
---
##  **Geometrías de escala de un solo nodo 3D o de todos los nodos de la escena 3D**
Los desarrolladores pueden escalar solo las geometrías de un nodo 3D o todos los nodos de 3D Scene. Para lograr esto, los desarrolladores pueden llamar a varios miembros de Scale de la instancia de la clase `PolygonModifier`. Este es el ejemplo de código para escalar todos los nodos o un solo nodo:



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
