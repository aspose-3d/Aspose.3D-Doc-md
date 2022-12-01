---
title: Adding Transformation to the Node
type: docs
weight: 10
url: /java/adding-transformation-to-the-node/
description: Aspose.3D for Java API has support to rotate objects in 3D space. There are three ways to define object’s rotation in 3D space, Euler angles, Quaternion and Custom Matrix, all of them are supported by the Transform class.
---

{{% alert color="primary" %}} 

Aspose.3D for Java API has support to rotate objects in 3D space. There are three ways to define object’s rotation in 3D space, Euler angles, Quaternion and Custom Matrix, all of them are supported by the `Transform` class.

{{% /alert %}} 

TSR (Translation/Scaling/Rotation) are most commonly used in 3D scenario, we provided a class `Transform` to access these in Aspose.3D Affine transformations include:

- Translation
- Scaling
- Rotation
- Shear mapping
- Squeeze mapping

{{% alert color="primary" %}} 

The `Mesh` class object is being used in the code. We can [create a Mesh class object as narrated there](https://docs.dynabic.com/display/3djava/Create+3D+Mesh+and+Scene).

{{% /alert %}} 
## **Rotate by Quaternion**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-AddTransformationToNodeByQuaternion.java" >}}
## **Rotate by Euler Angles**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-AddTransformationToNodeByEulerAngles.java" >}}
## **Custom Transformation Matrix**
We can also use Matrix directly:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-AddTransformationToNodeByTransformationMatrix.java" >}}
