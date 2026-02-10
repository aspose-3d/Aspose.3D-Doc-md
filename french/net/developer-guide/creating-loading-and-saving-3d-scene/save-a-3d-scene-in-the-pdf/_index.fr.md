---
title: Enregistrer une scène 3D dans le PDF dans C#
linktitle: Enregistrer une scène 3D dans le PDF
type: docs
weight: 60
url: /fr/net/save-a-3d-scene-in-the-pdf/
description: La classe Scene de Aspose.3D API représente une scène 3D. Les développeurs peuvent construire une scène 3D en ajoutant Caméra, Lumière, polygones et diverses autres entités. Ils peuvent également enregistrer une scène 3D au format PDF.
---
##  **Aperçu**

Cet article explique comment vous pouvez convertir le fichier 3D au format PDF en utilisant la manipulation de fichier C# .NET 3D et la conversion API, vous devez d'abord [Charger le fichier 3D dans l'objet Scène](https://docs.aspose.com/3d/net/create-and-read-an-existing-3d-scene/), puis l'enregistrer au format PDF. Il couvre un large éventail de sujets, par ex.

- Convertir 3D en PDF en C#
- Convertir FBX en PDF en C#
- Convertir STL en PDF en C#
- Convertir U3D en PDF en C#
- Convertir OBJ en PDF en C#

{{% alert color="primary" %}} 

La classe [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) de la scène Aspose.3D API représente une scène 3D. Les développeurs peuvent construire une scène 3D en ajoutant Caméra, Lumière, polygones et diverses autres entités. Ils peuvent également enregistrer une scène 3D dans le format de fichier PDF.

{{% /alert %}} {{% alert color="primary" %}} 

Aspose.3D for .NET écrit directement les informations sur le API et le numéro de version dans les documents de sortie. Par exemple, lors du rendu d'un dessin à PDF, Aspose.3D for .NET remplit le champ `Application` avec la valeur 'Aspose.3D' et `PDF Producer` champ avec valeur, e.g 'Aspose.3D 17.9'.

Veuillez noter que vous ne pouvez pas demander à Aspose.3D for .NET API de modifier ou de supprimer ces informations des documents de sortie.

{{% /alert %}} 
##  **Créer un 3D PDF avec un cylindre, et rendu en mode illustration ombré avec CAD éclairage optimisé**
La méthode Save de la classe `Scene` permet de sauvegarder une scène 3D au format PDF. Les développeurs peuvent charger n'importe quel fichier pris en charge 3D ou créer une nouvelle scène 3D, ils peuvent enregistrer une scène 3D au format PDF comme indiqué dans cet exemple de code C#:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET

            // Create a new scene
            Scene scene = new Scene();
            // Create a cylinder child node
            scene.RootNode.CreateChildNode("cylinder", new Cylinder()).Material = new PhongMaterial() { DiffuseColor = new Vector3(Color.DarkCyan) };
            // Set rendering mode and lighting scheme
            PdfSaveOptions opt = new PdfSaveOptions();
            opt.LightingScheme = PdfLightingScheme.CAD;
            opt.RenderMode = PdfRenderMode.ShadedIllustration;
            // Save in the PDF format
            scene.Save("output_out.pdf", opt);

{{< /highlight >}}
