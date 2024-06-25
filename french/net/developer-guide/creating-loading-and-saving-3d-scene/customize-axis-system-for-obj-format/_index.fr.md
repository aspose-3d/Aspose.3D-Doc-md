---
title: Personnaliser le système d'axe pour le format obj
linktitle: Personnaliser le système d'axes lors de l'exportation de la scène au format OBJ
type: docs
weight: 70
url: /fr/net/customize-axis-system-for-obj-format
description: OBJ n'a pas de système de coordonnées par défaut, nous pouvons définir manuellement le système d'axe pour cela.
---
{{% alert color="primary" %}} 

Les fichiers Wavefront OBJ n'adhèrent pas à un système de coordonnées standard; l'interprétation est généralement gérée par l'importateur. Cependant, [Aspose.3D for .NET](https://products.aspose.com/3d/net/) offre la possibilité de spécifier manuellement un système d'axes pour les fichiers OBJ. Cela comprend la définition des axes haut et avant ainsi que la sélection entre les systèmes de coordonnées gauchers et droitiers. Aspose.3D gérera automatiquement la conversion du système de coordonnées, assurant la cohérence et la précision de vos modèles 3D.


{{% /alert %}} 
##  **Spécification du système d'axe pour OBJ Fichiers dans Aspose.3D**

Voici comment définir manuellement le système d'axes lorsque vous travaillez avec des fichiers OBJ dans Aspose.3D:

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

En utilisant la configuration du système d'axe de Aspose.3D pour les fichiers OBJ, vous pouvez obtenir des résultats d'importation cohérents et précis quel que soit le système de coordonnées d'origine utilisé dans le fichier OBJ. Cette fonctionnalité améliore la flexibilité et le contrôle, ce qui facilite l'intégration et le travail avec les fichiers OBJ dans divers flux de travail 3D.

##  **Ressources**

1. [Tutoriel en ligne](https://products.aspose.com/3d/tutorial/)
2. [AxisSystem](https://reference.aspose.com/3d/net/aspose.threed/axissystem/)