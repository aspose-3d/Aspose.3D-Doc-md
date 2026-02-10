---
title: Encodage du maillage 3D dans le fichier Google Draco
type: docs
weight: 30
url: /fr/java/encoding-3d-mesh-in-the-google-draco-file/
description: Aspose.3D for Java API supporte l'importation du modèle 3D, la récupération du maillage, puis l'encodage du maillage dans le fichier Google Draco.
---
{{% alert color="primary" %}} 

Aspose.3D for Java API supporte l'importation du modèle 3D, la récupération du maillage, puis l'encodage du maillage dans le fichier Google Draco. Les développeurs peuvent également spécifier la position, les coordonnées de texture, la couleur et les bits normaux ainsi que le niveau de compression avant de coder un maillage.

{{% /alert %}} 
##  **Récupérer 3D Mesh et Encode dans le fichier Google Draco**
La méthode d'encode exposée par la classe `DracoFormat` peut être utilisée pour encoder un maillage 3D dans le fichier Google Draco. Il prend des objets `Mesh` et `DracoSaveOptions` comme paramètres. Avec les options de sauvegarde Draco, les développeurs peuvent également spécifier la position, les coordonnées de texture, la couleur et les bits normaux ainsi que le niveau de compression avant de coder un maillage.
###  **Échantillon de programmation**
Cet exemple de code récupère Mesh of Sphere, puis encode dans le fichier Google Draco après avoir spécifié un niveau de compression.

{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// Create a sphere
Sphere sphere = new Sphere();
// Encode the sphere to Google Draco raw data using optimal compression level.
DracoSaveOptions opt = new DracoSaveOptions();
opt.setCompressionLevel(DracoCompressionLevel.OPTIMAL);
byte[] b = FileFormat.DRACO.encode(sphere.toMesh(), opt);
// Save the raw bytes to file
Files.write(Paths.get(MyDir, "SphereMeshtoDRC_Out.drc"), b);
{{< /highlight >}}
