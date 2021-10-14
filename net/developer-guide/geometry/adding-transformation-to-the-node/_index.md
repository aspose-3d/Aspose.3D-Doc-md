---
title: Adding Transformation to the Node
type: docs
weight: 30
url: /net/adding-transformation-to-the-node/
---

{{% alert color="primary" %}}

Aspose.3D for .NET offers to rotate objects in 3D space. There are three ways to define object’s rotation in 3D space, Euler angles, Quaternion and Custom Matrix, all of them are supported by the [Transform](http://www.aspose.com/api/net/3d/T_Aspose_ThreeD_Transform) class.

{{% /alert %}}

TSR (Translation/Scaling/Rotation) are most commonly used in 3D scenario, we provided a class [Transform](http://www.aspose.com/api/net/3d/T_Aspose_ThreeD_Transform) to access these in Aspose.3D. Affine transformations include:

- Translation
- Scaling
- Rotation
- Shear mapping
- Squeeze mapping

{{% alert color="primary" %}}

The [Mesh](https://apireference.aspose.com/3d/net/aspose.threed.entities/mesh) class object is being used in the code. We can [create a Mesh class object as narrated there](/3d/net/create-3d-mesh-and-scene/).

{{% /alert %}}
## **Rotate by Quaternion**
{{< gist "aspose-3d" "631532eeb21c3374f2ed" "Examples-CSharp-Geometry-and-Hierarchy-TransformationToNodeByQuaternion-AddTransformationToNodeByQuaternion.cs" >}}
## **Rotate by Euler Angles**
{{< gist "aspose-3d" "631532eeb21c3374f2ed" "Examples-CSharp-Geometry-and-Hierarchy-TransformationToNodeByEulerAngles-AddTransformationToNodeByEulerAngles.cs" >}}
## **Custom Transformation Matrix**
We can also use Matrix directly:

{{< gist "aspose-3d" "631532eeb21c3374f2ed" "Examples-CSharp-Geometry-and-Hierarchy-TransformationToNodeByTransformationMatrix-AddTransformationToNodeByTransformationMatrix.cs" >}}
