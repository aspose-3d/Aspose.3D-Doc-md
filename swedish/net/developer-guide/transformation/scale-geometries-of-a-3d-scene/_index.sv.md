---
title: Skal geometrier för en 3D Scene
type: docs
weight: 70
url: /sv/net/scale-geometries-of-a-3d-scene/
description: Utvecklare kan endast skala geometrier för en 3D nod eller alla noder i 3D Scen. För att uppnå detta, kan utvecklare ringa flera Scale medlemmar av PolygonModifier klass instans.
---
##  **Skala geometrier för en enda 3D nod eller alla noder för 3D Scene**
Utvecklare kan endast skala geometrier för en 3D nod eller alla noder i 3D Scen. För att uppnå detta, kan utvecklare ringa flera Scale-medlemmar i `PolygonModifier` klassinstansen. Detta är kodexemplet för att skala alla noder eller enstaka nod:



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
