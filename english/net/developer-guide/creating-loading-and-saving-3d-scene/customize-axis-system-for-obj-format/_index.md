---
title: Customize axis system for obj format
linktitle: Customize axis system during exporting scene into OBJ format
type: docs
weight: 70
url: /net/customize-axis-system-for-obj-format
description: OBJ have no default coordinate system, we can manually define axis system for it.
---

{{% alert color="primary" %}} 

Wavefront OBJ files do not adhere to a standard coordinate system; instead, the interpretation is typically handled by the importer. However, [Aspose.3D for .NET](https://products.aspose.com/3d/net/) provides the flexibility to manually specify an axis system for OBJ files. This includes defining the up and front axes as well as selecting between left-handed and right-handed coordinate systems. Aspose.3D will automatically handle the coordinate system conversion, ensuring consistency and accuracy in your 3D models.


{{% /alert %}} 
## **Specifying Axis System for OBJ Files in Aspose.3D**

Here’s how you can manually set the axis system when working with OBJ files in Aspose.3D:

{{< highlight csharp >}}
//construct a right-handed axis system with +y as up and -z as front
Axis up = Axis.YAxis;
Axis front = Axis.NegativeZAxis;
AxisSystem axisSystem = new AxisSystem(CoordinateSystem.RightHanded, up, front);

ObjSaveOptions opt = new ObjSaveOptions();
//use the custom axis system to flip coordinate
opt.AxisSystem = axisSystem;
//set this to true, will convert mesh's position/normal from source axis system to custom axis system
//source axis system is defined by scene.AssetInfo.CoordinateSystem, scene.AssetInfo.UpVector, scene.AssetInfo.FrontVector
opt.FlipCoordinateSystem = true;

 // initialize a new 3D scene from existing file

var scene = Scene.FromFile("input.dae");

// Save the scene with customized axis system
s.Save("output.obj", opt);

{{< /highlight >}}

By using Aspose.3D's axis system configuration for OBJ files, you can achieve consistent and accurate import results regardless of the original coordinate system used in the OBJ file. This feature enhances flexibility and control, making it easier to integrate and work with OBJ files in diverse 3D workflows.

## **Resources**

1. [Online Tutorial](https://products.aspose.com/3d/tutorial/)
2. [AxisSystem](https://reference.aspose.com/3d/net/aspose.threed/axissystem/)