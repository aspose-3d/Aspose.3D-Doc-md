---
title: Encodage 3D Maille dans le fichier Google Draco
type: docs
weight: 30
url: /fr/java/encoding-3d-mesh-in-the-google-draco-file/
description: Aspose.3D for Java API a la charge d'importer le modèle 3D, de récupérer le maillage, puis d'encoder le maillage dans le fichier Google Draco.
---
{{% alert color="primary" %}} 

Aspose.3D for Java API a la charge d'importer le modèle 3D, de récupérer le maillage, puis d'encoder le maillage dans le fichier Google Draco. Les développeurs peuvent également spécifier la position, les coordonnées de texture, la couleur et les bits normaux ainsi que le niveau de compression avant d'encoder un maillage.

{{% /alert %}} 
## **Récupérer 3D Maille et code dans le fichier Google Draco**
La méthode d'encode exposée par la classe `DracoFormat` peut être utilisée pour coder un maillage 3D dans le fichier Google Draco. Il faut un `Mesh` et `DracoSaveOptions` objets comme paramètres. Avec les options de sauvegarde Draco, les développeurs peuvent également spécifier la position, les coordonnées de texture, la couleur et les bits normaux ainsi que le niveau de compression avant d'encoder un maillage.
### **Échantillon de programmation**
Cet exemple de code récupère Mesh of Sphere, puis encode dans le fichier Google Draco après avoir spécifié un niveau de compression.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-objects-Encode3DMeshinGoogleDraco.java" >}}
