---
title: Achsen system für das obj-Format anpassen
linktitle: Achsen system während des Exports der Szene in das OBJ-Format anpassen
type: docs
weight: 70
url: /de/net/customize-axis-system-for-obj-format
description: OBJ haben kein Standard koordinaten system, wir können das Achsen system dafür manuell definieren.
---
{{% alert color="primary" %}} 

Wavefront OBJ-Dateien entsprechen nicht einem Standard-Koordinaten system. Stattdessen wird die Interpretation normaler weise vom Importeur übernommen. [Aspose.3D for .NET](https://products.aspose.com/3d/net/) bietet jedoch die Flexibilität, ein Achsen system für OBJ-Dateien manuell anzugeben. Dies beinhaltet die Definition der Hoch-und Vorderachse sowie die Auswahl zwischen Links-und Rechtshänder-Koordinaten systemen. Aspose.3D übernimmt automatisch die Konvertierung des Koordinaten systems, um sicher zustellen, dass Ihre 3D Modelle konsistent und genau sind.


{{% /alert %}} 
##  **Festlegen des Axis-Systems für OBJ-Dateien in Aspose.3D**

So können Sie das Achsen system manuell einstellen, wenn Sie mit OBJ-Dateien in Aspose.3D arbeiten:

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

Durch die Verwendung der Achsen system konfiguration von Aspose.3D für OBJ-Dateien können Sie konsistente und genaue Import ergebnisse erzielen, unabhängig vom ursprünglichen Koordinaten system, das in der OBJ-Datei verwendet wird. Diese Funktion verbessert die Flexibilität und Kontrolle und erleichtert die Integration und Arbeit mit OBJ-Dateien in verschiedenen 3D-Workflows.

##  **Ressourcen**

1. [Online-Tutorial](https://products.aspose.com/3d/tutorial/)
2. [Achsensystem](https://reference.aspose.com/3d/net/aspose.threed/axissystem/)