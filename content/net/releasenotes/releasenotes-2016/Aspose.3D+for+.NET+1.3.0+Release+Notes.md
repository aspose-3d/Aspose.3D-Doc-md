+++
title = "Aspose.3D for .NET 1.3.0 Release Notes" 
description = "" 
weight = 12149 
+++

Aspose.3D for .NET : Aspose.3D for .NET 1.3.0 Release Notes  

# Aspose.3D for .NET : Aspose.3D for .NET 1.3.0 Release Notes


## Other Improvements and Changes

{{< table style="table-striped" >}}
|Key|Summary|Category|
|:----|:----|:----|
|THREEDNET-127|Reading support of Universal 3D format.|New Feature|
|THREEDNET-133|Verify Aspose.3D namespaces conform to Microsoft guidelines.|Enhancement|
|THREEDNET-130|Fix Aspose license abuse issue possibly caused by Aspose Ventures.|Bug|
{{< /table >}}

### Public API and Backwards Incompatible Changes

See the list for any changes made to the public API such as added, renamed, removed or deprecated members as well as any non-backward compatible change made to Aspose.3D for .NET. If you have concerns about any change listed, please raise it on the [Aspose.3D support forum](http://www.aspose.com/community/forums/aspose.3d-product-family/535/showforum.aspx).

#### Namespace and class name changes:

*   Namespace Aspose.ThreeD.Animations changed to Aspose.ThreeD.Animation
*   Class Aspose.ThreeD.Animations.Animation changed to Aspose.ThreeD.Animation.AnimationNode
*   Namespace Aspose.ThreeD.IO changed to Aspose.ThreeD.Formats
*   Namespace Aspose.ThreeD.Utils changed to Aspose.ThreeD.Utilities

#### Functional changes:

*   Added a Decompose method on Matrix4
*   Allow user to decompose transform matrix to translation/scaling/rotation/skew/perspective.
*   Added a new Constructor on Vector4 to receive a Vector3 parameter.
*   Make it easier to construct a Vector4 based on a Vector3.
*   Added a new overloads for Geometry.CreateElement and Geometry.CreateElementUV
*   Allows user to create a new vertex element and assign reference mode/mapping mode at once, to make code shorter.
*   Changed LayeredTexture.Textures' type from ICollection to IList
*   Allow user to access the layered textures by index.
*   Added Content property in Texture
*   Allow user to embed raw texture data inside the Texture instance for FBX files.

#### Create Vertex by Assigning the Reference and Mapping Modes

Developers can create vertex by assigning the Reference and Mapping modes in a single line of code. Example code: [Set up normals or UV on the Cube](https://docs2.aspose.com/3d/net/developerguide/geometry/set+up+normals+or+uv+on+the+cube+and+add+material+to+3d+entities).

#### Universal 3D Saving Option is added in the FileFormat

The Universal 3D format option has been added in the FileFormat enum.

#### Embed Raw Content to the Texture of FBX

The <tt>Content</tt> property has added to the <tt>Texture</tt> class to embed the raw content in the texture of FBX document. Example code: [Add material to the cube](http://www.aspose.com/docs/display/3dnet/Set+up+normals+or+UV+on+the+Cube+and+Add+material+to+the+cube#SetupnormalsorUVontheCubeandAddmaterialtothecube-Addmaterialtothecube).

#### Decompose method is added in the Matrix4 class

It is a mathematical utility function used to decompose an affine transformation matrix.

#### A new constructor in Vector4 class is added to receive a Vector3 object parameter

It makes easier to construct a Vector4 based on the Vector3. The fourth value of the Vector4 presents plane w and its default value is 1.

