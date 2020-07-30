---
title : "Add an Asset Information and Flip Coordinate System in 3D Formats" 
description : "" 
weight : 12032 
toc : false
type: docs
url: /net/developerguide/workingwith3dscene/add+an+asset+information+and+flip+coordinate+system+in+3d+formats/
---

# Aspose.3D for .NET : Add an Asset Information and Flip Coordinate System in 3D Formats


{{< panel title="Contents Summary" style="primary" >}}
*   1 [Add an Asset Information to 3D Scene](#add-an-asset-information-to-3d-scene)
    *   1.1 [Define a Metadata for the scene](#define-a-metadata-for-the-scene)
*   2 [Flip Coordinate System in 3D Formats](#flip-coordinate-system-in-3d-formats)
{{< /panel >}}
 

 

## Add an Asset Information to 3D Scene

Metadata is structured information that describes, explains, locates or makes it easier to retrieve, use or manage an information resource. Aspose.3D for .NET API allows developers to define a Metadata for the scene.

### Define a Metadata for the scene

3D shows produce massive qunatities of metadata and picture information. Metadata is an asset and part of the show.

1.  Initialize a 3D Scene using [Scene](#) class.
2.  Set application/tool name.
3.  Set application/tool vendor name.
4.  Set measurement unit.
5.  Set measurement unit scale factor.
6.  Save 3D scene in the supported file format.

In this example, we assume the scene is created by a CAD tool called “Egypt” and it’s designed by “Manualdesk”:

## Flip Coordinate System in 3D Formats

Aspose.3D for .NET API allows users to flip coordinate system in the OBJ, 3DS, STL and U3D formats.

To import a 3ds file and save it in OBJ format the [Scene](http://www.aspose.com/api/net/3d/T_Aspose_ThreeD_Scene) class is being used in the code.

In this example, we flipped the coordinate system while importing the 3ds file, and saved it in OBJ format without materials.

