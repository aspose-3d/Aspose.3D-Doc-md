+++
title = "Add Animation Property and Setup Target Camera in 3D document" 
description = "" 
weight = 12037 
+++

Aspose.3D for .NET : Add Animation Property and Setup Target Camera in 3D document  

# Aspose.3D for .NET : Add Animation Property and Setup Target Camera in 3D document


{{< panel title="Contents Summary" style="primary" >}}
*   1 [Add Animation property in 3D document](#AddAnimationPropertyandSetupTargetCamerain3Ddocument-AddAnimationpropertyin3Ddocument)
    *   1.1 [Move Cube’s Position](#AddAnimationPropertyandSetupTargetCamerain3Ddocument-MoveCube’sPosition)
*   2 [Setup the Target Camera in 3D File](#AddAnimationPropertyandSetupTargetCamerain3Ddocument-SetuptheTargetCamerain3DFile)
{{< /panel >}}
 

 

## Add Animation property in 3D document

Aspose.3D for .NET supports rendering animated scene. This article explains prerequisites to move an object.

### Move Cube’s Position

The [Mesh](http://www.aspose.com/api/net/3d/T_Aspose_ThreeD_Entities_Mesh) class object is being used in the code. We can [create a Mesh class object as narrated there](https://docs2.aspose.com/3d/net/developerguide/creatingloadingandsaving3dscene/create+and+read+an+existing+3d+scene) and it's must animate the local translation property of the node too: [Adding the Transformation to the Node](https://docs2.aspose.com/3d/net/developerguide/geometry/adding+transformation+to+the+node).

In Aspose.3D, object animation is actually key-frame animation that animates on properties. To animate properties, you need a CurveMapping instance which maps components of a property to different curves, for example, a Vector3 property can have 3 components X/Y/Z, which will set up three channels in CurveMapping, every channel can have a set of Curves.

## Setup the Target Camera in 3D File

Aspose.3D for .NET offers to setup the target camera in 3D file. In some file formats, light/camera supports target, which allows the light/camera always facing a specified node, this is useful in animation.

The [Scene](http://www.aspose.com/api/net/3d/T_Aspose_ThreeD_Scene), [Camera](http://www.aspose.com/api/net/3d/T_Aspose_ThreeD_Entities_Camera), [Node](http://www.aspose.com/api/net/3d/T_Aspose_ThreeD_Node) and [Transform](http://www.aspose.com/api/net/3d/T_Aspose_ThreeD_Transform) classes are being used in the code. To save a Scene, [Scene.Save](http://www.aspose.com/api/net/3d/M_Aspose_ThreeD_Scene_Save) method is being used, it accepts a file name with complete path and [FileFormat](http://www.aspose.com/api/net/3d/T_Aspose_ThreeD_FileFormat) parameter.

In below example, the target and camera is setup in 3D file:

