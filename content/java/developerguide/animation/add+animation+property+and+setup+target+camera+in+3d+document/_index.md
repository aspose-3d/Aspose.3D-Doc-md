---
title : "Add Animation Property and Setup Target Camera in 3D document" 
description : "" 
weight : 12035 
toc : false
type: docs
url: /java/developerguide/animation/add+animation+property+and+setup+target+camera+in+3d+document/
---

# Aspose.3D for Java : Add Animation Property and Setup Target Camera in 3D document


{{< panel title="Contents Summary" style="primary" >}}
*   1 [Add Animation property in 3D document](#add-animation-property-in-3d-document)
    *   1.1 [Move Cube’s Position](#move-cube’s-position)
*   2 [Setup the Target Camera in 3D File](#setup-the-target-camera-in-3d-file)
{{< /panel >}}
 

 

## Add Animation property in 3D document

Aspose.3D for Java supports rendering animated scene. This article explains prerequisites to move an object.

### Move Cube’s Position

The **Mesh** class object is being used in the code. We can [create a Mesh class object as narrated there](https://docs.dynabic.com/display/3djava/Create+3D+Mesh+and+Scene) and it's must animate the local translation property of the node too: [Adding the Transformation to the Node](https://docs.dynabic.com/display/3djava/Adding+Transformation+to+the+Node).

In Aspose.3D for Java API, animation instance is actually key-frame animation that animates on properties. In order animate properties, you need a CurveMapping instance which maps components of a property to different curves, for example, a Vector3 property can have 3 components X/Y/Z, which will set up three channels in CurveMapping, every channel can have a set of Curves.

## Setup the Target Camera in 3D File

Aspose.3D for .NET offers to setup the target camera in 3D file. In some file formats, light/camera supports target, which allows the light/camera always facing a specified node, this is useful in animation.

The **Scene**, **Camera**, **Node** and **Transform** classes are being used in the code. in order to save a Scene, **Scene.save** method is being used, it accepts a file name with complete path and **FileFormat** parameter.

In below example, the target and camera is setup in 3D file:

