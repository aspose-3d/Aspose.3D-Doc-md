---
title: Importer 3D Scènes et contenus d'un PDF
type: docs
weight: 50
url: /fr/python-net/import-3d-scenes-and-contents-from-a-pdf/
description: La classe Scene de Aspose.3D API représente une scène 3D. Les développeurs peuvent extraire des scènes 3D et le contenu d'un fichier PDF.
---
{{% alert color="primary" %}}

La classe [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) de la scène Aspose.3D API représente une scène 3D. Les développeurs peuvent extraire 3D scènes et le contenu d'un fichier PDF.

{{% /alert %}}
##  **Ouvrir une scène à partir d'un mot de passe protégé PDF**
La méthode `open` de la classe `Scene` permet de charger la scène 3D à partir d'un fichier d'entrée PDF. Les développeurs peuvent également appliquer un mot de passe pour les fichiers PDF protégés en utilisant la classe [`PdfLoadOptions`](https://reference.aspose.com/3d/net/aspose.threed.formats/pdfloadoptions) comme indiqué dans cet exemple de code:

{{< highlight "python" >}}
from aspose.threed import Scene
from aspose.threed.formats import PdfLoadOptions

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Create a new scene
scene = Scene()
options = PdfLoadOptions()
options.password = "password".encode("utf-8")
#  Use loading options and apply password
opt = options
#  Open scene
scene.open("data-dir"  + "House_Design.pdf", opt)

{{< /highlight >}}
##  **Extraire tout le contenu brut 3D d'un PDF**
La méthode `extract` de la classe [`PdfFormat`](https://reference.aspose.com/3d/net/aspose.threed.formats/pdfformat) permet d'extraire le contenu 3D d'un fichier PDF. Les développeurs peuvent parcourir le contenu et les enregistrer dans des fichiers séparés comme indiqué dans cet exemple de code:

{{< highlight "python" >}}
from aspose.threed import FileFormat

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  The path to the documents directory.
password = None
#  Extract 3D contents
contents = FileFormat.PDF.extract("data-dir"  + "House_Design.pdf", password)
i = 1
#  Iterate through the contents and in separate 3D files
for content in contents:
    fileName = "3d-"  + str(i)
    i = i + 1
    with open(fileName, "wb") as f:
        f.write(content)

{{< /highlight >}}
##  **Extraire toutes les scènes 3D et les enregistrer dans les formats 3D pris en charge**
La méthode `extract_scene` de la classe `PdfFormat` permet d'extraire des scènes 3D d'un fichier PDF. Les développeurs peuvent parcourir les scènes et les enregistrer dans les formats de fichier 3D pris en charge, comme indiqué dans cet exemple de code:

{{< highlight "python" >}}
from aspose.threed import FileFormat

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
password = None
scenes = FileFormat.PDF.extract_scene("data-dir"  + "House_Design.pdf", password)
i = 1
#  Iterate through the scenes and save in 3D files
for scene in scenes:
    fileName = "3d-"  + str(i) + ".fbx"
    i = i + 1
    scene.save("out"  + fileName, FileFormat.FBX7400ASCII)

{{< /highlight >}}

{{% alert color="primary" %}}

Tous les formats de fichier 3D pris en charge sont répertoriés dans la page [Aperçu du produit](/3d/fr/python-net/product-overview/).

{{% /alert %}}
