---
title: Add Animation Property and Setup Target Camera in 3D document
type: docs
weight: 10
url: /net/add-animation-property-and-setup-target-camera-in-3d-document/
---

## **Add Animation property in 3D document**
Aspose.3D for .NET supports rendering animated scene. This article explains prerequisites to move an object.
### **Move Cube’s Position**
{{% alert color="primary" %}}

The [Mesh](https://apireference.aspose.com/3d/net/aspose.threed.entities/mesh) class object is being used in the code. We can [create a Mesh class object as narrated there](/3d/net/create-and-read-an-existing-3d-scene/) and it's must animate the local translation property of the node too: [Adding the Transformation to the Node](/3d/net/adding-transformation-to-the-node/).

{{% /alert %}}

In Aspose.3D, object animation is actually key-frame animation that animates on properties. To animate properties, you need a CurveMapping instance which maps components of a property to different curves, for example, a Vector3 property can have 3 components X/Y/Z, which will set up three channels in CurveMapping, every channel can have a set of Curves.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Animation-PropertyToDocument-AddAnimationPropertyToDocument.cs" >}}
## **Setup the Target Camera in 3D File**
Aspose.3D for .NET offers to setup the target camera in 3D file. In some file formats, light/camera supports target, which allows the light/camera always facing a specified node, this is useful in animation.

{{% alert color="primary" %}}

The [Scene](https://apireference.aspose.com/3d/net/aspose.threed/scene), [Camera](https://apireference.aspose.com/3d/net/aspose.threed.entities/camera), [Node](https://apireference.aspose.com/3d/net/aspose.threed/node) and [Transform](https://apireference.aspose.com/3d/net/aspose.threed/transform) classes are being used in the code. To save a Scene, [Scene.Save](https://apireference.aspose.com/3d/net/aspose.threed/scene/methods/save) method is being used, it accepts a file name with complete path and [FileFormat](https://apireference.aspose.com/3d/net/aspose.threed/fileformat) parameter.

{{% /alert %}}

In below example, the target and camera is setup in 3D file:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Animation-SetupTargetAndCamera-SetupTargetAndCamera.cs" >}}
