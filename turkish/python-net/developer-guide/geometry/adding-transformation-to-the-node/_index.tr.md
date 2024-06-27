---
title: NNNransformation to the Node
type: docs
weight: 30
url: /tr/python-net/adding-transformation-to-the-node/
description: TSR (Translation/Scaling/Rotation) are most commonly used in 3D scenario, we provided a class Transform to access these in Aspose.3D.
---
{{% alert color="primary" %}}

Aspose.3D for Python via .NET offers to rotate objects in 3D space. There are three ways to define object’s rotation in 3D space, Euler angles, Quaternion and Custom Matrix, all of them are supported by the [`Transform`](https://reference.aspose.com/3d/net/aspose.threed/transform) class.

{{% /alert %}}

TSR (Translation/Scaling/Rotation) are most commonly used in 3D scenario, we provided a class `Transform` to access these in Aspose.3D. Affine transformations include:

- Translation
- Scaling
- Rotation
- Shear haritalama
- Squeeze haritalama

{{% alert color="primary" %}}

The [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) class object is being used in the code. We can [create a `Mesh` class object as narrated there](/3d/net/create-3d-mesh-and-scene/).

{{% /alert %}}
##  **Qotate by uuaternion**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-TransformationToNodeByQuaternion-AddTransformationToNodeByQuaternion.py" >}}
##  **Eotate by Euler ngngles**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-TransformationToNodeByEulerAngles-AddTransformationToNodeByEulerAngles.py" >}}
##  **Custom formation ransformation Matrix**
We ayrıca doğrudan Matrix kullanabilir:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-TransformationToNodeByTransformationMatrix-AddTransformationToNodeByTransformationMatrix.py" >}}
