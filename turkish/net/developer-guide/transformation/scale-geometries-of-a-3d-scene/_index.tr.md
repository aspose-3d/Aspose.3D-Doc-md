---
title: 3D sahnesinin ölçekli geometrileri
type: docs
weight: 70
url: /tr/net/scale-geometries-of-a-3d-scene/
description: Geliştiriciler sadece 3D düğümünün veya 3D sahnesinin tüm düğümlerinin geometrilerini ölçebilir. Bunu başarmak için, geliştiriciler polygonmodifier sınıf örneğinin birden fazla ölçekli üyesini arayabilir.
---
##  **Tek bir 3D düğümünün veya 3D sahnesinin tüm düğümlerinin ölçekli geometrileri**
Developers can scale only geometries of a 3D node or all nodes of 3D Scene. In order to achieve this, developers can call multiple Scale members of the `PolygonModifier` class instance. This is the code example to scale all nodes or single node:



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
