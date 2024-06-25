---
title: Geometrien einer 3D-Szene skalieren
type: docs
weight: 70
url: /de/net/scale-geometries-of-a-3d-scene/
description: Entwickler können nur Geometrien eines 3D-Knotens oder aller Knoten der 3D-Szene skalieren. Um dies zu erreichen, können Entwickler mehrere Scale-Mitglieder der PolygonModifier-Klassen instanz aufrufen.
---
##  **Skalieren Sie Geometrien eines einzelnen 3D-Knotens oder aller Knoten der 3D-Szene**
Entwickler können nur Geometrien eines 3D-Knotens oder aller Knoten der 3D-Szene skalieren. Um dies zu erreichen, können Entwickler mehrere Scale-Mitglieder der `PolygonModifier`-Klassen instanz aufrufen. Dies ist das Code beispiel, um alle Knoten oder einzelnen Knoten zu skalieren:



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
