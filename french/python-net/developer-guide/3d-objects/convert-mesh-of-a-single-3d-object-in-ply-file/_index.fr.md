---
title: Convertir le maillage d'un seul objet 3D dans un fichier PLY
type: docs
weight: 20
url: /fr/python-net/convert-mesh-of-a-single-3d-object-in-ply-file/
description: Les membres EncodeMesh surchargés exposés par la classe PlyFormat peuvent être utilisés pour convertir le maillage d'un objet 3D en fichier PLY. Les membres EncodeMesh prennent les objets Mesh, le nom du fichier de sortie et PlySaveOptions comme paramètres. En utilisant les options de sauvegarde PLY, les développeurs peuvent changer le nom des composants de coordonnées.
---
{{% alert color="primary" %}}

[Aspose.3D for Python via .NET](https://products.aspose.com/3d/python-net/) API permet aux développeurs de convertir le maillage d'un seul objet 3D dans le fichier PLY.

{{% /alert %}}
##  **Créez un objet 3D et enregistrez-le dans le fichier PLY**
Les membres `encodeMesh` surchargés exposés par la classe `PlyFormat` peuvent être utilisés pour convertir le maillage d'un objet 3D en fichier PLY. Les membres `encodeMesh` prennent les objets `Mesh`, le nom du fichier de sortie et `PlySaveOptions` comme paramètres. En utilisant les options de sauvegarde PLY, les développeurs peuvent changer le nom des composants de coordonnées.
###  **Échantillon de programmation**
Cet exemple de code crée un objet 3D Cylinder, puis l'encode dans le fichier PLY.

**Python**

```py

from aspose.threed import FileFormat, FileContentType
from aspose.threed.entities import Cylinder
from aspose.threed.formats import PlySaveOptions

# Create a cylinder object and save it to ply file

FileFormat.PLY.encode_mesh(Cylinder(), "cylinder.ply")

# using Ply save options

# Save as binary PLY format, the default value is ASCII

opt = PlySaveOptions(FileContentType.BINARY)

# change the components to 's' and 't'

opt.texture_coordinate_components.item1 = "s
opt.texture_coordinate_components.item2 = "t"

# save the mesh

FileFormat.PLY.encode_mesh(Cylinder(), "cylinder.ply", opt)

```
