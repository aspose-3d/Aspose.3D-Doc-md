---
title: Add Animation Property and Setup Target Camera in 3D document
type: docs
weight: 10
url: /java/add-animation-property-and-setup-target-camera-in-3d-document/
---

## **Add Animation property in 3D document**
Aspose.3D for Java supports rendering animated scene. This article explains prerequisites to move an object.
### **Move Cube’s Position**
{{% alert color="primary" %}}

The **Mesh** class object is being used in the code. We can [create a Mesh class object as narrated there](https://docs.aspose.com/3d/java/create-3d-mesh-and-scene/) and it's must animate the local translation property of the node too: [Adding the Transformation to the Node](https://docs.aspose.com/3d/java/adding-transformation-to-the-node/).

{{% /alert %}}

In Aspose.3D for Java API, animation instance is actually key-frame animation that animates on properties. In order animate properties, you need a CurveMapping instance which maps components of a property to different curves, for example, a Vector3 property can have 3 components X/Y/Z, which will set up three channels in CurveMapping, every channel can have a set of Curves.

{{< gist "aspose-com-gists" "0672215ca08d7566bd64d657e2b228a7" "src-java-examples-animation-PropertyToDocument-AddAnimationPropertyToDocument.java" >}}
## **Setup the Target Camera in 3D File**
Aspose.3D for .NET offers to setup the target camera in 3D file. In some file formats, light/camera supports target, which allows the light/camera always facing a specified node, this is useful in animation.

{{% alert color="primary" %}}

The **Scene**, **Camera**, **Node** and **Transform** classes are being used in the code. in order to save a Scene, **Scene.save** method is being used, it accepts a file name with complete path and **FileFormat** parameter.

{{% /alert %}}

In below example, the target and camera is setup in 3D file:

{{< gist "aspose-3d" "a10c42b56128eaadb7d7f81e2176306c" "aspose-3d-src-examples-animation-SetupTargetAndCamera.java" >}}
