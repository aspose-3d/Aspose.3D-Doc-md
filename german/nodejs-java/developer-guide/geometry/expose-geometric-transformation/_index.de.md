---
title: Expose Geometrische Transformation
type: docs
weight: 50
url: "/de/nodejs-java/expose-geometric-transformation/"
description: "Aspose.3D für Node.js über Java ermöglicht die Darstellung von geometrischen Transformationen einer 3D-Szene. Sie können die globale Transformation mit der Methode evaluateGlobalTransform auswerten."
---

# **Geometrische Transformation freigeben**
Aspose.3D für Node.js via Java ermöglicht die Freigabe der geometrischen Transformation einer 3D-Szene. Sie können die globale Transformation mithilfe der Methode `evaluateGlobalTransform` auswerten. Der folgende Codeausschnitt zeigt, wie die geometrische Transformation freigegeben wird.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// Initialisiere Szenenobjekt
var scene = new aspose.threed.Scene();

// Initialisiere Zylinder
var cylinder =new aspose.threed.Cylinder();

// Erstelle ChildNode
var Node=scene.getRootNode().createChildNode(cylinder);

// Hole geometrische Translation
Node.getTransform().setGeometricTranslation(new aspose.threed.Vector3(10, 0, 0));

// Die erste Console.WriteLine gibt die Transformationsmatrix aus, die die geometrische Transformation enthält
// während die zweite dies nicht tut.
console.log(Node.evaluateGlobalTransform(true));
console.log(Node.evaluateGlobalTransform(false));

{{< /highlight >}}