---
title: Encodage du maillage 3D dans le fichier Google Draco
type: docs
weight: 60
url: /fr/python-net/encoding-3d-mesh-in-the-google-draco-file/
description: Aspose.3D for Python via .NET API permet aux développeurs d'importer un modèle 3D, puis d'encoder des maillages dans les fichiers Google Draco. Les développeurs peuvent également spécifier la position, les coordonnées de texture, la couleur et les bits normaux ainsi que le niveau de compression avant de coder un maillage.
---
{{% alert color="primary" %}}

[Aspose.3D for Python via .NET](https://products.aspose.com/3d/python-net/) API permet aux développeurs de [Importer un modèle 3D](/3d/fr/net/create-and-read-an-existing-3d-scene/#createandreadanexisting3dscene-readinga3dscene), puis d'encoder les maillages dans les fichiers Google Draco. Les développeurs peuvent également spécifier la position, les coordonnées de texture, la couleur et les bits normaux ainsi que le niveau de compression avant de coder un maillage.

{{% /alert %}}
##  **Récupérer un maillage 3D et Encode dans un fichier Google Draco**
La méthode `encode` exposée par la classe [`DracoFormat`](https://reference.aspose.com/net/3d/aspose.threed.formats/dracoformat) peut être utilisée pour encoder un maillage 3d dans le fichier Google Draco. Il prend des objets [`Mesh`](https://reference.aspose.com/net/3d/aspose.threed.entities/mesh) et [`DracoSaveOptions`](https://reference.aspose.com/net/3d/aspose.threed.formats.draco/dracosaveoptions) comme paramètres. En utilisant les options de sauvegarde Draco, les développeurs peuvent également spécifier la position, les coordonnées de texture, la couleur et les bits normaux ainsi que le niveau de compression avant de coder un maillage.
###  **Échantillon de programmation**
Cet exemple de code récupère un maillage de sphère, puis l'encode dans le fichier Google Draco après avoir spécifié un niveau de compression.

{{< highlight "python" >}}
from aspose.threed import FileFormat
from aspose.threed.entities import Sphere
from aspose.threed.formats import DracoCompressionLevel, DracoSaveOptions

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Create a sphere
sphere = Sphere()
options = DracoSaveOptions()
options.compression_level = DracoCompressionLevel.OPTIMAL
#  Encode the sphere to Google Draco raw data using optimal compression level.
b = FileFormat.DRACO.encode(sphere.to_mesh(), options)
#  Save the raw bytes to file
with open("out"  + "SphereMeshtoDRC_Out.drc", "wb") as f:
    f.write(b)

{{< /highlight >}}
