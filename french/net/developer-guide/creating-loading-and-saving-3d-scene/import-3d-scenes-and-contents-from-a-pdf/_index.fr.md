---
title: Importer 3D Scènes et contenu d'un PDF dans C#
linktitle: Importer 3D Scènes et contenus d'un PDF
type: docs
weight: 50
url: /fr/net/import-3d-scenes-and-contents-from-a-pdf/
keywords: 3d pdf, 3d pdf c#
description: La classe Scene de Aspose.3D API représente une scène 3D. Les développeurs peuvent extraire des scènes 3D et le contenu d'un fichier PDF.
---
{{% alert color="primary" %}}

La classe [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) de la scène Aspose.3D API représente une scène 3D. Les développeurs peuvent extraire 3D scènes et le contenu d'un fichier PDF.

{{% /alert %}}
##  **Ouvrir une scène à partir d'un mot de passe protégé PDF**
La méthode `Open` de la classe `Scene` permet de charger la scène 3D à partir d'un fichier d'entrée PDF. Les développeurs peuvent également appliquer un mot de passe pour les PDF protégés en utilisant la classe [`PdfLoadOptions`](https://reference.aspose.com/3d/net/aspose.threed.formats/pdfloadoptions) comme indiqué dans cet exemple de code C#:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-OpenSceneFromProtectedPdf-OpenSceneFromProtectedPdf.cs" >}}
##  **Extraire tout le contenu brut 3D d'un PDF**
La méthode Extract de la classe [`PdfFormat`](https://reference.aspose.com/3d/net/aspose.threed.formats/pdfformat) permet d'extraire le contenu 3D d'un fichier PDF. Les développeurs peuvent parcourir le contenu et les enregistrer dans les fichiers séparés comme indiqué dans cet exemple de code C#:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-ExtractRaw3DContentsFromPdf-ExtractRaw3DContentsFromPdf.cs" >}}
##  **Extraire toutes les scènes 3D et les enregistrer dans les formats 3D pris en charge**
La méthode `ExtractScene` de la classe `PdfFormat` permet d'extraire des scènes 3D d'un fichier PDF. Les développeurs peuvent parcourir les scènes et les enregistrer dans les formats de fichier 3D pris en charge, comme indiqué dans cet exemple de code C#:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-ExtractAll3DScenes-ExtractAll3DScenes.cs" >}}

{{% alert color="primary" %}}

Tous les formats de fichier 3D pris en charge sont répertoriés dans la page [Aperçu du produit](/3d/fr/net/product-overview/).

{{% /alert %}}
