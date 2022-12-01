---
title: Personnaliser la conversion de matériaux non-PBR en PBR avant de sauver les scènes 3D au format GLTF 2.0
type: docs
weight: 50
url: /fr/java/customize-non-pbr-to-pbr-materials-conversion-before-saving-3d-scenes-to-gltf-2-0-format/
description: La classe Scène du Aspose.3D for Java API représente une scène 3D et les développeurs peuvent construire une scène 3D en ajoutant diverses entités.
---
{{% alert color="primary" %}} 

La classe `Scene` du Aspose.3D for Java API représente une scène 3D et les développeurs peuvent construire une scène 3D en ajoutant diverses entités. GLTF 2.0 prend uniquement en charge les matériaux PBR (rendu à base physique), Aspose.3D API convertit en interne les matériaux non PBR en matériaux PBR avant d'être exportés en GLTF 2.0 (les matériaux de la scène resteront inchangés pendant l'exportation), et les développeurs peuvent fournir une fonction de conversion personnalisée pour remplacer le comportement par défaut.

{{% /alert %}} 
## **Conversion de matériaux non-PBR vers PBR**
Cet exemple de code montre comment convertir du matériel en matériel PBR, puis enregistre la scène 3D au format GLTF:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-Non_PBRtoPBRMaterial.java" >}}
