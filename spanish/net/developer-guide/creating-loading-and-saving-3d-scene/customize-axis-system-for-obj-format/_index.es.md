---
title: Personalizar el sistema de ejes para el formato obj
linktitle: Personalizar el sistema de ejes durante la exportación de escena en formato OBJ
type: docs
weight: 70
url: /es/net/customize-axis-system-for-obj-format
description: OBJ no tienen un sistema de coordenadas predeterminado, podemos definir manualmente el sistema de ejes para él.
---
{{% alert color="primary" %}} 

Los archivos Wavefront OBJ no se adhieren a un sistema de coordenadas estándar; en su lugar, la interpretación es normalmente manejada por el importador. Sin embargo, [Aspose.3D for .NET](https://products.aspose.com/3d/net/) proporciona la flexibilidad de especificar manualmente un sistema de ejes para los archivos OBJ. Esto incluye definir los ejes superior y frontal, así como seleccionar entre sistemas de coordenadas zurdos y diestros. Aspose.3D manejará automáticamente la conversión del sistema de coordenadas, asegurando consistencia y precisión en sus modelos 3D.


{{% /alert %}} 
##  **Especificación del sistema de ejes para archivos OBJ en Aspose.3D**

A continuación se explica cómo puede configurar manualmente el sistema de ejes cuando se trabaja con archivos OBJ en Aspose.3D:

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

Al utilizar la configuración del sistema de ejes de Aspose.3D para archivos OBJ, puede obtener resultados de importación coherentes y precisos independientemente del sistema de coordenadas original utilizado en el archivo OBJ. Esta característica mejora la flexibilidad y el control, lo que facilita la integración y el trabajo con archivos OBJ en diversos flujos de trabajo 3D.

##  **Recursos**

1. [Tutorial en línea](https://products.aspose.com/3d/tutorial/)
2. [Sistema AxisSystem](https://reference.aspose.com/3d/net/aspose.threed/axissystem/)