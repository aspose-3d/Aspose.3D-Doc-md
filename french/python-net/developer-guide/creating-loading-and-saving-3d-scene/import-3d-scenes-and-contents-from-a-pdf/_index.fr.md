---
title: Importer 3D Scènes et contenus à partir d'un PDF
type: docs
weight: 50
url: /fr/python-net/import-3d-scenes-and-contents-from-a-pdf/
description: La classe Scène du Aspose.3D API représente une scène 3D. Les développeurs peuvent extraire les scènes et le contenu 3D d'un fichier PDF.
---
{{% alert color="primary" %}}

La classe [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) du Aspose.3D API représente une scène 3D. Les développeurs peuvent extraire les scènes et le contenu 3D d'un fichier PDF.

{{% /alert %}}
## **Scène ouverte à partir d'un mot de passe protégé PDF**
La méthode `open` de la classe `Scene` permet de charger la scène 3D à partir d'un fichier d'entrée PDF. Les développeurs peuvent également appliquer le mot de passe pour les PDF protégés en utilisant la classe [`PdfLoadOptions`](https://reference.aspose.com/3d/net/aspose.threed.formats/pdfloadoptions) comme indiqué dans cet exemple de code:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-OpenSceneFromProtectedPdf-OpenSceneFromProtectedPdf.py" >}}
## **Extraire tout cru 3D Contenu d'un PDF**
La méthode `extract` de la classe [`PdfFormat`](https://reference.aspose.com/3d/net/aspose.threed.formats/pdfformat) permet d'extraire le contenu 3D d'un fichier PDF. Les développeurs peuvent itérer à travers le contenu, et les enregistrer dans les fichiers séparés comme indiqué dans cet exemple de code:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-ExtractRaw3DContentsFromPdf-ExtractRaw3DContentsFromPdf.py" >}}
## **Extrayez toutes les scènes 3D et sauvegardez-les dans les formats 3D pris en charge**
La méthode `extract_scene` de la classe `PdfFormat` permet d'extraire des scènes 3D d'un fichier PDF. Les développeurs peuvent itérer à travers les scènes, et les enregistrer dans les formats de fichier 3D pris en charge comme indiqué dans cet exemple de code:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-ExtractAll3DScenes-ExtractAll3DScenes.py" >}}

{{% alert color="primary" %}}

Tous les formats de fichier 3D pris en charge sont listés dans le[Aperçu du produit](/3d/fr/python-net/product-overview/)Page.

{{% /alert %}}
