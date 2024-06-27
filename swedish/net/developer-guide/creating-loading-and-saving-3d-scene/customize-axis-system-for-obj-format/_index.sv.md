---
title: Anpassa axelsystem för obj-format
linktitle: Anpassa axelsystem under export av scen i formatet OBJ.
type: docs
weight: 70
url: /sv/net/customize-axis-system-for-obj-format
description: OBJ har inget standardkoordinatsystem, vi kan manuellt definiera axelsystem för det.
---
{{% alert color="primary" %}} 

Wavefront OBJ filer följer inte ett standardiserat koordinatsystem. Istället hanteras vanligtvis av importören. [Aspose.3D for .NET](https://products.aspose.com/3d/net/) ger dock flexibilitet att manuellt ange ett axesystem för OBJ filer. Detta inbegriper att definiera upp- och främre axlar samt att välja mellan vänsterhända och högerhända koordinatsystem. Aspose. 3D hanterar automatiskt konverteringen av koordinatsystemet, vilket säkerställer enhetlighet och noggrannhet i 3D-modellerna.


{{% /alert %}} 
##  **Ange axelsystem för OBJ Filer i Aspose.3D**

Här är hur du kan ställa in axelsystemet manuellt när du arbetar med OBJ-filer i Aspose.3D:

{{< highlight "csharp" >}}
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

Genom att använda Aspose. 3D axissysteminställning för OBJ filer, du kan uppnå konsekventa och korrekta importresultat oavsett det ursprungliga koordinatsystemet som används i filen OBJ. Denna funktion ökar flexibiliteten och kontrollen. gör det lättare att integrera och arbeta med OBJ filer i olika 3D arbetsflöden.

##  **Resurser**

1. [Online Tutorial](https://products.aspose.com/3d/tutorial/)
2. [AxisSystemName](https://reference.aspose.com/3d/net/aspose.threed/axissystem/) 2