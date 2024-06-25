---
title: 缩放 3D 场景的几何图形
type: docs
weight: 70
url: /zh/net/scale-geometries-of-a-3d-scene/
description: 开发人员只能缩放 3D 节点或 3D 场景的所有节点的几何图形。为了实现这一点，开发人员可以调用PolygonModifier类实例的多个Scale成员。
---
##  **缩放单个 3D 节点或 3D 场景的所有节点的几何图形**
开发人员只能缩放 3D 节点或 3D 场景的所有节点的几何图形。为了实现这一点，开发人员可以调用 `PolygonModifier` 类实例的多个Scale成员。这是缩放所有节点或单个节点的代码示例:



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
