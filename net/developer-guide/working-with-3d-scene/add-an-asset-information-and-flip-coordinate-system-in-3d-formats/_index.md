---
title: Add an Asset Information and Flip Coordinate System in 3D Formats
type: docs
weight: 10
url: /net/add-an-asset-information-and-flip-coordinate-system-in-3d-formats/
description: Metadata is structured information that describes, explains, locates or makes it easier to retrieve, use or manage an information resource. Aspose.3D for .NET API allows developers to define a Metadata for the scene.
---

## **Add an Asset Information to 3D Scene**
Metadata is structured information that describes, explains, locates or makes it easier to retrieve, use or manage an information resource. Aspose.3D for .NET API allows developers to define a Metadata for the scene.
### **Define a Metadata for the scene**
3D shows produce massive quantities of metadata and picture information. Metadata is an asset and part of the show.

1. Initialize a 3D Scene using [Scene](https://reference.aspose.com/3d/net/aspose.threed/scene) class.
1. Set application/tool name.
1. Set application/tool vendor name.
1. Set measurement unit.
1. Set measurement unit scale factor.
1. Save 3D scene in the supported file format.

In this example, we assume the scene is created by a CAD tool called “Egypt” and it’s designed by “Manualdesk”:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-AssetInformation-InformationToScene-AddAssetInformationToScene.cs" >}}
## **Flip Coordinate System in 3D Formats**
Aspose.3D for .NET API allows users to flip coordinate system in the OBJ, 3DS, STL and U3D formats.

{{% alert color="primary" %}} 

To import a 3ds file and save it in OBJ format the [Scene](https://reference.aspose.com/3d/net/aspose.threed/scene) class is being used in the code.

{{% /alert %}} 

In this example, we flipped the coordinate system while importing the 3ds file, and saved it in OBJ format without materials.
