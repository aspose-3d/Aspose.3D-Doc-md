---
title: Créer une scène avec des formes primitives 3D
type: docs
weight: 10
url: /fr/net/create-scene-with-primitive-3d-shapes/
description: En utilisant Aspose.3D for .NET, les développeurs peuvent définir une scène avec des formes primitives 3D. Toutes les primitives paramétrées seront converties en maillage automatiquement tout en sauvegardant dans n'importe quel format de fichier de sortie pris en charge.
---
{{% alert color="primary" %}}

En utilisant [Aspose.3D for .NET](https://products.aspose.com/3d/net/), les développeurs peuvent définir une scène avec des formes primitives 3D. Toutes les primitives paramétrées seront converties en maillage automatiquement tout en sauvegardant dans n'importe quel format de fichier de sortie pris en charge.

{{% /alert %}}
##  **Construire une scène à partir de formes primitives 3D**
La modélisation est le processus de création pure et Aspose.3D API supporte la création d'une scène avec des formes primitives 3D.
###  **Échantillon de programmation**
Cet exemple de code crée une scène avec des formes primitives 3D et enregistre dans le fichier FBX.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET

// Initialize a Scene object
Scene scene = new Scene();
// Create a Box model
scene.RootNode.CreateChildNode("box", new Box());
// Create a Cylinder model
scene.RootNode.CreateChildNode("cylinder", new Cylinder());
// Save drawing in the FBX format
scene.Save("test.fbx");


{{< /highlight >}}
