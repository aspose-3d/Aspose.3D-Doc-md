---
title: Économisez une scène 3D dans le PDF à C#
linktitle: Économisez une scène 3D dans le PDF
type: docs
weight: 60
url: /fr/net/save-a-3d-scene-in-the-pdf/
description: La classe Scène du Aspose.3D API représente une scène 3D. Les développeurs peuvent créer une scène 3D en ajoutant une caméra, une lumière, des polygones et diverses autres entités. Ils peuvent également maintenant enregistrer une scène 3D au format de fichier PDF.
---
## **Aperçu**

Cet article explique comment vous pouvez convertir le fichier 3D au format PDF en utilisant C# .NET 3D manipulation et conversion API, vous devez d'abord[Charge le fichier 3D dans l'objet Scène](https://docs.aspose.com/3d/net/create-and-read-an-existing-3d-scene/)Puis sauvegardez-le au format PDF. Il couvre un large éventail de sujets, par ex.

- Convertissez 3D en PDF
- Convertissez FBX en PDF
- Convertissez STL en PDF
- Convertissez U3D en PDF
- Convertissez OBJ en PDF

{{% alert color="primary" %}} 

La classe [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) du Aspose.3D API représente une scène 3D. Les développeurs peuvent créer une scène 3D en ajoutant une caméra, une lumière, des polygones et diverses autres entités. Ils peuvent également maintenant enregistrer une scène 3D dans le format de fichier PDF.

{{% /alert %}} {{% alert color="primary" %}} 

Aspose.3D for .NET écrit directement les informations sur le API et le numéro de version dans les documents de sortie. Par exemple, lors du rendu d'un dessin à PDF, Aspose.3D for .NET remplit le champ `Application` d'une valeur 'Aspose.3D' et `PDF Producer` avec une valeur, par exemple 'Aspose.3D 17,9 '.

Veuillez noter que vous ne pouvez pas indiquer au Aspose.3D for .NET API de modifier ou de supprimer ces informations des documents de sortie.

{{% /alert %}} 
## **Créer un 3D PDF avec un cylindre et rendu en mode d'illustration ombrée avec un éclairage optimisé CAD**
La méthode Save de la classe `Scene` permet d'enregistrer une scène 3D au format PDF. Les développeurs peuvent charger n'importe quel fichier pris en charge par 3D ou créer une nouvelle scène 3D, ils peuvent enregistrer une scène 3D au format PDF comme indiqué dans cet exemple de code C#:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-Save3DInPdf-Save3DInPdf.cs" >}}
