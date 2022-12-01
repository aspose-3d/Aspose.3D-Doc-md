---
title: Personnaliser la conversion de matériaux non-PBR en PBR avant de sauver les scènes 3D au format GLTF 2.0 au format C#
linktitle: Personnaliser la conversion de matériaux non-PBR en PBR avant de sauver les scènes 3D au format GLTF 2.0
type: docs
weight: 70
url: /fr/net/customize-non-pbr-to-pbr-materials-conversion-before-saving-3d-scenes-to-gltf-2-0-format/
description: La classe Scène du Aspose.3D API représente une scène 3D. Les développeurs peuvent déjà construire une scène 3D en ajoutant diverses entités. Le GLTF 2.0 prend uniquement en charge les matériaux PBR (rendu à base physique), le Aspose.3D API convertit en interne les matériaux non PBR en matériaux PBR avant l'exportation en GLTF 2.0.
---
{{% alert color="primary" %}} 

La classe [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) du Aspose.3D API représente une scène 3D. Les développeurs peuvent déjà construire une scène 3D en ajoutant diverses entités. GLTF 2.0 prend uniquement en charge les matériaux PBR (rendu à base physique), Aspose.3D API convertit en interne les matériaux non PBR en matériaux PBR avant d'exporter en GLTF 2.0 (les matériaux de la scène resteront inchangés pendant l'exportation), et les développeurs peuvent fournir une fonction de conversion personnalisée pour remplacer le comportement par défaut.

{{% /alert %}} 
## **Conversion de matériaux non-PBR vers PBR**
Cet exemple de code C# montre comment convertir du matériel en matériel PBR, puis enregistre la scène 3D au format GLTF avec C# 3D 3D manipulation et conversion API:

**C#**

{{< highlight "java" >}}

 // initialize a new 3D scene

var s = new Scene();

var box = new Box();

s.RootNode.CreateChildNode("box1", box).Material = new PhongMaterial() {DiffuseColor = new Vector3(1, 0, 1)};

GLTFSaveOptions opt = new GLTFSaveOptions(FileFormat.GLTF2);

//Custom material converter to convert PhongMaterial to PbrMaterial

opt.MaterialConverter = delegate(Material material)

{

    PhongMaterial m = (PhongMaterial) material;

    return new PbrMaterial() {Albedo = new Vector3(m.DiffuseColor.x, m.DiffuseColor.y, m.DiffuseColor.z)};

};

// save in GLTF 2.0 format

s.Save("test.gltf", opt);

{{< /highlight >}}
