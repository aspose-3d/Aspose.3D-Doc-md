---
title: Expose Geometric Transformation
type: docs
weight: 50
url: /nodejs-java/expose-geometric-transformation/
description: Aspose.3D for Node.js via Java allows exposing geometric transformation of a 3D scene. You can evaluate the global transformation using evaluateGlobalTransform method.
---

# **Expose Geometric Transformation**
Aspose.3D for Node.js via Java allows exposing geometric transformation of a 3D scene. You can evaluate the global transformation using `evaluateGlobalTransform` method. The following code snippet shows how to expose the geometric transformation.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Initialize scene object
var scene = new aspose.threed.Scene();

// Initialize cylinder
var cylinder =new aspose.threed.Cylinder();

// Create ChildNode
var Node=scene.getRootNode().createChildNode(cylinder);

// Get Geometric Translation
Node.getTransform().setGeometricTranslation(new aspose.threed.Vector3(10, 0, 0));

// The first Console.WriteLine will output the transform matrix that includes the geometric transformation
// while the second one will not.
console.log(Node.evaluateGlobalTransform(true));
console.log(Node.evaluateGlobalTransform(false));

{{< /highlight >}}
