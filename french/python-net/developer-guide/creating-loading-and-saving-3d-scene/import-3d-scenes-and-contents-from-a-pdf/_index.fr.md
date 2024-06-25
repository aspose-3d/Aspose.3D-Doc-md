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

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-OpenSceneFromProtectedPdf-OpenSceneFromProtectedPdf.py" >}}
##  **Extraire tout le contenu brut 3D d'un PDF**
La méthode `extract` de la classe [`PdfFormat`](https://reference.aspose.com/3d/net/aspose.threed.formats/pdfformat) permet d'extraire le contenu 3D d'un fichier PDF. Les développeurs peuvent parcourir le contenu et les enregistrer dans des fichiers séparés comme indiqué dans cet exemple de code:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-ExtractRaw3DContentsFromPdf-ExtractRaw3DContentsFromPdf.py" >}}
##  **Extraire toutes les scènes 3D et les enregistrer dans les formats 3D pris en charge**
La méthode `extract_scene` de la classe `PdfFormat` permet d'extraire des scènes 3D d'un fichier PDF. Les développeurs peuvent parcourir les scènes et les enregistrer dans les formats de fichier 3D pris en charge, comme indiqué dans cet exemple de code:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-ExtractAll3DScenes-ExtractAll3DScenes.py" >}}

{{% alert color="primary" %}}

Tous les formats de fichier 3D pris en charge sont répertoriés dans la page [Aperçu du produit](/3d/fr/python-net/product-overview/).

{{% /alert %}}
