---
title: Geometrie in scala di una scena 3D
type: docs
weight: 70
url: /it/net/scale-geometries-of-a-3d-scene/
description: Gli sviluppatori possono scalare solo le geometrie di un nodo 3D o tutti i nodi della scena 3D. Per raggiungere questo obiettivo, gli sviluppatori possono chiamare più membri Scale dell'istanza della classe PolygonModifier.
---
## **Geometrie di scala di un singolo nodo 3D o di tutti i nodi della scena 3D**
Gli sviluppatori possono scalare solo le geometrie di un nodo 3D o tutti i nodi della scena 3D. Per raggiungere questo obiettivo, gli sviluppatori possono chiamare più membri Scale dell'istanza della classe `PolygonModifier`. Questo è l'esempio di codice per scalare tutti i nodi o singolo nodo:



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
