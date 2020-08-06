---
title: Public API Changes in Aspose.3D 1.3.0
type: docs
weight: 40
url: /net/public-api-changes-in-aspose-3d-1-3-0/
---

**Contents Summary**

- [Namespace and class name changes](#PublicAPIChangesinAspose.3D1.3.0-Namespaceandclassnamechanges)
- [Create Vertex by Assigning the Reference and Mapping Modes](#PublicAPIChangesinAspose.3D1.3.0-CreateVertexbyAssigningtheReferenceandMappingModes)
- [Universal 3D Saving Option is added in the FileFormat](#PublicAPIChangesinAspose.3D1.3.0-Universal3DSavingOptionisaddedintheFileFormat)
- [Embed Raw Content to the Texture of FBX](#PublicAPIChangesinAspose.3D1.3.0-EmbedRawContenttotheTextureofFBX)
- [Decompose method is added in the Matrix4 class](#PublicAPIChangesinAspose.3D1.3.0-DecomposemethodisaddedintheMatrix4class)
- [A new constructor in Vector4 class is added to receive a Vector3 object parameter](#PublicAPIChangesinAspose.3D1.3.0-AnewconstructorinVector4classisaddedtoreceiveaVector3objectparameter)

{{% alert color="primary" %}} 

This document describes changes to the Aspose.3D API from version 1.2.0 to 1.3.0, that may be of interest to module/application developers. It includes not only new and updated public methods, but also a description of any changes in the behavior behind the scenes in Aspose.3D.

{{% /alert %}} 
### **Namespace and class name changes**
- Namespace Aspose.ThreeD.Animations changed to Aspose.ThreeD.Animation
- Class Aspose.ThreeD.Animations.Animation changed to Aspose.ThreeD.Animation.AnimationNode
- Namespace Aspose.ThreeD.IO changed to Aspose.ThreeD.Formats
- Namespace Aspose.ThreeD.Utils changed to Aspose.ThreeD.Utilities
### **Create Vertex by Assigning the Reference and Mapping Modes**
Developers can create vertex by assigning the Reference and Mapping modes in a single line of code. Example code:

{{% alert color="primary" %}} 

The Mesh class object is being used in the code. We can [create a Mesh class object as narrated there](/pages/createpage.action?spaceKey=3dnet&title=Create+a+3D+Cube+Mesh&linkCreation=true&fromPageId=19923253).

{{% /alert %}} 

**C#**

{{< highlight csharp >}}

 // call overloaded CreateElement method of the Mesh object

VertexElementNormal elementNormal = mesh.CreateElement(VertexElementType.Normal, MappingMode.ControlPoint, ReferenceMode.Direct) as VertexElementNormal;

{{< /highlight >}}

Error rendering macro 'code' : Invalid value specified for parameter lang
### **Universal 3D Saving Option is added in the FileFormat**
The Universal 3D format option has been added in the FileFormat enum. Example code:

**C#**

{{< highlight csharp >}}

 // save scene in the Universal3D format

scene.Save("C:\\temp\\Output.fbx", FileFormat.Universal3D);

{{< /highlight >}}

Error rendering macro 'code' : Invalid value specified for parameter lang
### **Embed Raw Content to the Texture of FBX**
The <tt>Content</tt> property has added to the <tt>Texture</tt> class to embed the raw content in the texture of FBX document. Example code:

**C#**

{{< highlight csharp >}}

 // initialize Texture class object

Texture texture = new Texture();

// set file name

texture.FileName = "embedded-texture.png";

// set binary content

texture.Content = File.ReadAllBytes("c:\\test.png");

{{< /highlight >}}

Error rendering macro 'code' : Invalid value specified for parameter lang
### **Decompose method is added in the Matrix4 class**
It is a mathematical utility function used to decompose an affine transformation matrix.
### **A new constructor in Vector4 class is added to receive a Vector3 object parameter**
It makes easier to construct a Vector4 based on the Vector3. The fourth value of the Vector4 presents plane w and its default value is 1.
