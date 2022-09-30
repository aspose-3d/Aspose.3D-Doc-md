---
title: 3D场景的比例几何
type: docs
weight: 70
url: /zh/net/scale-geometries-of-a-3d-scene/
description: 开发人员只能缩放3D节点的几何形状或3D场景的所有节点。为了实现这一点，开发人员可以调用polygonmodifidifier类实例的多个Scale成员。
---
## **单个3D节点或3D场景的所有节点的缩放几何形状**
开发人员只能缩放3D节点的几何形状或3D场景的所有节点。为了实现这一点，开发人员可以调用`PolygonModifier`类实例的多个规模成员。这是缩放所有节点或单个节点的代码示例:



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
