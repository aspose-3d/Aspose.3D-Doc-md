---
title: Масштабная геометрия сцены 3D
type: docs
weight: 70
url: /ru/net/scale-geometries-of-a-3d-scene/
description: Разработчики могут масштабировать только геометрию узла 3D или всех узлов сцены 3D. Чтобы достичь этого, разработчики могут вызывать несколько членов Scale экземпляра класса PolygonModifier.
---
##  **Масштабная геометрия одного узла 3D или всех узлов сцены 3D**
Разработчики могут масштабировать только геометрию узла 3D или всех узлов сцены 3D. Чтобы достичь этого, разработчики могут вызывать несколько членов Scale экземпляра класса `PolygonModifier`. Это пример кода для масштабирования всех узлов или одного узла:



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
