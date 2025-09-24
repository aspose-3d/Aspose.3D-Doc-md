---
title: Adding Transformation to the Node
type: docs
weight: 10
url: /nodejs-java/adding-transformation-to-the-node/
description: "Aspose.3D for Node.js via Java API has support to rotate objects in 3D space. There are three ways to define object's rotation in 3D space, Euler angles, Quaternion and Custom Matrix, all of them are supported by the Transform class."
---

{{% alert color="primary" %}} 

Aspose.3D for Node.js via Java API has support to rotate objects in 3D space. There are three ways to define object’s rotation in 3D space, Euler angles, Quaternion and Custom Matrix, all of them are supported by the `Transform` class.

{{% /alert %}} 

TSR (Translation/Scaling/Rotation) are most commonly used in 3D scenario, we provided a class `Transform` to access these in Aspose.3D Affine transformations include:

- Translation
- Scaling
- Rotation
- Shear mapping
- Squeeze mapping

## **Rotate by Euler Angles**

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// Initialize scene object
var scene = new aspose.threed.Scene();

// Initialize cylinder
var cylinder =new aspose.threed.Cylinder(2, 2, 10, 20, 1, false);

// Create ChildNode
var Node=scene.getRootNode().createChildNode(cylinder);

// Euler angles
Node.getTransform().setEulerAngles(new aspose.threed.Vector3(30, 40, 50));

// Set translation
Node.getTransform().setTranslation(new aspose.threed.Vector3(0, 0, 20));

// Save
scene.save("TransformationToNode.obj");

{{< /highlight >}}

## **Custom Transformation Matrix**
We can also use Matrix directly:

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// Initialize scene object
var scene = new aspose.threed.Scene();

// Initialize cylinder
var cylinder =new aspose.threed.Cylinder(2, 2, 10, 20, 1, false);

// Create ChildNode
var Node=scene.getRootNode().createChildNode(cylinder);

// Set custom translation matrix
Node.getTransform().setTransformMatrix(new aspose.threed.Matrix4(
    1, -0.3, 0, 0,
    0.4, 1, 0.3, 0,
    0, 0, 1, 0,
    0, 20, 0, 1
));

// Save
scene.save("TransformationToNode.obj");

{{< /highlight >}}
