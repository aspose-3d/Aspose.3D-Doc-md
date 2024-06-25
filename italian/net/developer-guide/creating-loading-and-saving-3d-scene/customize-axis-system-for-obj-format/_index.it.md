---
title: Personalizzare il sistema di assi per il formato obj
linktitle: Personalizzare il sistema degli assi durante l'esportazione della scena in formato OBJ
type: docs
weight: 70
url: /it/net/customize-axis-system-for-obj-format
description: OBJ non hanno un sistema di coordinate predefinito, possiamo definire manualmente il sistema degli assi.
---
{{% alert color="primary" %}} 

I file Wavefront OBJ non sono conformi a un sistema di coordinate standard; invece, l'interpretazione viene in genere gestita dall'importatore. Tuttavia, [Aspose.3D for .NET](https://products.aspose.com/3d/net/) offre la flessibilità di specificare manualmente un sistema di assi per OBJ file. Ciò include la definizione degli assi su e davanti, nonché la selezione tra i sistemi di coordinate mancini e destrorsi. Aspose.3D gestirà automaticamente la conversione del sistema di coordinate, garantendo coerenza e precisione nei tuoi modelli da 3D.


{{% /alert %}} 
##  **Specifica del sistema Axis per OBJ file in Aspose.3D**

Ecco come impostare manualmente il sistema degli assi quando si lavora con OBJ file in Aspose.3D:

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

Utilizzando la configurazione del sistema dell'asse Aspose.3D per i file OBJ, è possibile ottenere risultati di importazione coerenti e accurati indipendentemente dal sistema di coordinate originale utilizzato nel file OBJ. Questa funzione migliora la flessibilità e il controllo, semplificando l'integrazione e il lavoro con i file OBJ in diversi flussi di lavoro 3D.

##  **Risorse**

1. [Tutorial online](https://products.aspose.com/3d/tutorial/)
2. [Sistema AxisSystem](https://reference.aspose.com/3d/net/aspose.threed/axissystem/)