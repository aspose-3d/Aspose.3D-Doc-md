---
title: Encodage 3D Maille dans le fichier Google Draco
type: docs
weight: 60
url: /fr/python-net/encoding-3d-mesh-in-the-google-draco-file/
description: Aspose.3D pour Python via .NET API permet aux développeurs d'importer un modèle 3D, puis d'encoder des maillages dans les fichiers Google Draco. Les développeurs peuvent également spécifier la position, les coordonnées de texture, la couleur et les bits normaux ainsi que le niveau de compression avant d'encoder un maillage.
---
{{% alert color="primary" %}}

[Aspose.3D pour Python via .NET](https://products.aspose.com/3d/python-net/)API permet aux développeurs de[Importer un modèle 3D](/3d/fr/net/create-and-read-an-existing-3d-scene/#createandreadanexisting3dscene-readinga3dscene), Puis codez les maillages dans les fichiers Google Draco. Les développeurs peuvent également spécifier la position, les coordonnées de texture, la couleur et les bits normaux ainsi que le niveau de compression avant d'encoder un maillage.

{{% /alert %}}
## **Récupérer une maille 3D et un code dans le fichier Google Draco**
La méthode `encode` exposée par la classe [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat) peut être utilisée pour coder un maillage 3D dans le fichier Google Draco. Il faut un [`Mesh`](https://reference.aspose.com/net/3d/aspose.threed.entities/mesh) et [`DracoSaveOptions`](https://reference.aspose.com/net/3d/aspose.threed.formats.draco/dracosaveoptions) objets comme paramètres. En utilisant les options de sauvegarde Draco, les développeurs peuvent également spécifier la position, les coordonnées de texture, la couleur et les bits normaux ainsi que le niveau de compression avant d'encoder un maillage.
### **Échantillon de programmation**
Cet exemple de code récupère une maille de sphère, puis encode dans le fichier Google Draco après avoir spécifié un niveau de compression.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-Encode3DMeshinGoogleDraco-Encode3DMeshinGoogleDraco.py" >}}
