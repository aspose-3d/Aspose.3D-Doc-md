---
title: Scale geometrileri 3D cene cene
type: docs
weight: 70
url: /tr/net/scale-geometries-of-a-3d-scene/
description: Developers sadece 3D düğümünün veya 3D cene cene tüm düğümlerinin geometrilerini ölçebilir. In bunu başarmak için, geliştiriciler olyolygongonodifier sınıf örneğinin birden fazla Scale üyesini arayabilir.
---
## **Tek bir 3D düğümünün veya 3D Scene tüm düğümlerinin Scale geometrileri**
Developers sadece 3D düğümünün veya 3D cene cene tüm düğümlerinin geometrilerini ölçebilir. In bunu başarmak için, geliştiriciler `PolygonModifier` sınıf örneğinin birden fazla Scale üyesini arayabilir. This, tüm düğümleri veya tek düğümleri ölçeklendirmek için kod örneğidir:



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
