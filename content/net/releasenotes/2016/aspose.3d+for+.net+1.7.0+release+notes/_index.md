---
title : "Aspose.3D for .NET 1.7.0 Release Notes" 
description : "" 
weight : 12145 
toc : false
type: docs
url: /net/releasenotes/2016/aspose.3d+for+.net+1.7.0+release+notes/
---

# Aspose.3D for .NET : Aspose.3D for .NET 1.7.0 Release Notes


This page contains release notes for [Aspose.3D for .NET 1.7.0](https://www.nuget.org/packages/Aspose.3D/1.7.0)

## Other Improvements and Changes

{{< table style="table-striped" >}}
|Key|Summary|Category|
|:----|:----|:----|
|THREEDNET-141|Add support of converting STL to an image format.|New Feature|
|THREEDNET-169|Render the scene to a texture.|New Feature|
|THREEDNET-170|Add support of shadow.|New Feature|
|THREEDNET-174|Generate normal data from smoothing group.|New Feature|
|THREEDNET-179|Index out of range error occurred on loading a U3D file.|Bug|
{{< /table >}}

### Public API and Backwards Incompatible Changes

See the list for any changes made to the public API such as added, renamed, removed or deprecated members as well as any non-backward compatible change made to Aspose.3D for .NET. If you have concerns about any change listed, please raise it on the [Aspose.3D support forum](http://www.aspose.com/community/forums/aspose.3d-product-family/535/showforum.aspx).

#### Adds Aspose.ThreeD.Entities.Frustum class

A new class Frustum is added. Camera and Light were the subclasses of Entity class. In the version 1.7.0, these classes are inherited from Frustum and Frustum is inherited from Entity, since the properties Position, Up, LookAt, Direction, Target, NearPlane and FarPlane are extracted into Frustum.

#### Adds Aspose.ThreeD.ImageRenderOptions class

It allows developers to set various rendering options like background color, asset directory and enable/disable object shadow before converting a 3D file to image.

#### Adds multiple Render methods in Aspose.ThreeD.Scene class

It renders a 3D scene in given camera's perspective into specified image file format and size.

#### Adds MoveForward method in Aspose.ThreeD.Entities.Camera class

It moves forward the camera towards its orientation. A camera's orientation is specified by any of the Target/Direction/LookAt

*   **Target:** A target node in space, the camera will always look at this target whatever the target/camera has changed its position in space.
*   **LookAt:** A fixed position in space, the camera will always look at this position.
*   **Direction:** A direction vector, a camera's orientation is directly specified by this vector whatever its position is.

#### Adds CastShadows and ReceiveShadows members in Aspose.ThreeD.Entities.Geometry class

Some file formats can store shadow related settings in geometry like FBX, and they're also used in rendering.

#### Adds GenerateNormal method in Aspose.ThreeD.Entities.PolygonModifier class

It allows developers to generate normal data from Mesh instance, if VertexElementSmoothingGroup element was defined on the mesh, the generated normal data will get smoothed by the VertexElementSmoothingGroup.

#### Adds Concate method in Aspose.ThreeD.Utilities.Quaternion class

It allows developers to concatenate two rotation transformation into one represented in Quaternion.

#### Usage Examples

Please check the list of help topics added in the Aspose.3D Wiki docs:

*   [Render an Image of 3D Model from the Camera](http://www.aspose.com/docs/display/3dnet/Render+an+Image+of+3D+Model+from+the+Camera)
*   [Cast and Receive Shadows on 3D Geometries](http://www.aspose.com/docs/display/3dnet/Cast+and+Receive+Shadows+on+3D+Geometries)
*   [Generate Normal Data for All Meshes in a 3D File](http://www.aspose.com/docs/display/3dnet/Generate+Normal+Data+for+All+Meshes+in+a+3D+File)
*   [Combine Quaternions and Apply them on 3D Geometries](http://www.aspose.com/docs/display/3dnet/Combine+Quaternions+and+Apply+them+on+3D+Geometries)

