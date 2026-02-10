---
title: Encodage du maillage 3D dans le fichier Google Draco
type: docs
weight: 60
url: /fr/net/encoding-3d-mesh-in-the-google-draco-file/
description: Aspose.3D for .NET API permet aux développeurs d'importer un modèle 3D, puis d'encoder des maillages dans les fichiers Google Draco. Les développeurs peuvent également spécifier la position, les coordonnées de texture, la couleur et les bits normaux ainsi que le niveau de compression avant de coder un maillage.
---
{{% alert color="primary" %}}

[Aspose.3D for .NET](https://products.aspose.com/3d/net/) API permet aux développeurs de [Importer un modèle 3D](/3d/fr/net/create-and-read-an-existing-3d-scene/#createandreadanexisting3dscene-readinga3dscene), puis d'encoder les maillages dans les fichiers Google Draco. Les développeurs peuvent également spécifier la position, les coordonnées de texture, la couleur et les bits normaux ainsi que le niveau de compression avant de coder un maillage.

{{% /alert %}}
##  **Récupérer un maillage 3D et Encode dans un fichier Google Draco**
La méthode `Encode` exposée par la classe [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat) peut être utilisée pour encoder un maillage 3d dans le fichier Google Draco. Il prend des objets [`Mesh`](https://reference.aspose.com/net/3d/aspose.threed.entities/mesh) et [`DracoSaveOptions`](https://reference.aspose.com/net/3d/aspose.threed.formats.draco/dracosaveoptions) comme paramètres. En utilisant les options de sauvegarde Draco, les développeurs peuvent également spécifier la position, les coordonnées de texture, la couleur et les bits normaux ainsi que le niveau de compression avant de coder un maillage.
###  **Échantillon de programmation**
Cet exemple de code récupère un `Mesh` de `Sphere`, puis l'encode dans le fichier Google Draco après avoir spécifié un niveau de compression.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
            
// Create a sphere
var sphere = new Sphere();
// Encode the sphere to Google Draco raw data using optimal compression level.
var b = FileFormat.Draco.Encode(sphere.ToMesh(), 
    new DracoSaveOptions() { CompressionLevel = DracoCompressionLevel.Optimal });
// Save the raw bytes to file
File.WriteAllBytes(RunExamples.GetOutputFilePath("SphereMeshtoDRC_Out.drc"), b);

{{< /highlight >}}
