---
title: Personnaliser la conversion des matériaux non-PBR en PBR avant de sauvegarder 3D Scènes au format GLTF 2.0 dans C#
linktitle: Personnaliser la conversion des matériaux non-PBR en PBR avant de sauvegarder les scènes 3D au format GLTF 2.0
type: docs
weight: 70
url: /fr/net/customize-non-pbr-to-pbr-materials-conversion-before-saving-3d-scenes-to-gltf-2-0-format/
description: La classe Scene de Aspose.3D API représente une scène 3D. Les développeurs peuvent déjà construire une scène 3D en ajoutant diverses entités. GLTF 2.0 prend uniquement en charge les matériaux PBR (Physically Based Rendering), Aspose.3D API convertit en interne les matériaux non-PBR en matériaux PBR avant d'exporter vers GLTF 2.0.
---
{{% alert color="primary" %}} 

La classe [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) de la scène Aspose.3D API représente une scène 3D. Les développeurs peuvent déjà construire une scène 3D en ajoutant diverses entités. GLTF 2.0 ne prend en charge que les matériaux PBR (Physically Based Rendering), Aspose.3D API convertit en interne les matériaux non-PBR en matériaux PBR avant d'exporter en GLTF 2.0 (les matériaux de la scène resteront inchangés pendant l'exportation), et les développeurs peuvent fournir une fonction de conversion personnalisée pour remplacer le comportement par défaut.

{{% /alert %}} 
##  **Conversion de matériaux non-PBR vers PBR**
Cet exemple de code C# montre comment convertir du matériel en matériau PBR, puis enregistre la scène 3D au format GLTF avec la manipulation de fichier C# 3D et la conversion API:

**C#**

{{< highlight "java" >}}

 // initialize a new 3D scene

var s = new Scene();

var box = new Box();

s.RootNode.CreateChildNode("box1", box).Material = new PhongMaterial() {DiffuseColor = new Vector3(1, 0, 1)};

GLTFSaveOptions opt = new GLTFSaveOptions(FileFormat.GLTF2);

//Custom material converter to convert PhongMaterial to PbrMaterial

opt.MaterialConverter = (Material material) => {
    var pbr = PbrMaterial.FromMaterial(material);
    //customize your own PBR material here, you can get the original OBJ's material from the parameter mat.
    //to create a compatible material with obj2gltf, use following definition:
    pbr.MetallicFactor = 0;
    pbr.RoughnessFactor = 0.98;
    return pbr;
};

// save in GLTF 2.0 format

s.Save("test.gltf", opt);

{{< /highlight >}}


##  **Ressources**

1. [Tutoriel en ligne](https://products.aspose.com/3d/tutorial/use-phong-material-to-pbr-material/)
