---
title: Votre première application Aspose.3D
type: docs
weight: 30
url: /fr/net/your-first-aspose-3d-application/
description: Créez, modifiez et enregistrez votre premier fichier 3D dans tous les formats pris en charge en utilisant Aspose.3D for .NET pour faire l'expérience de sa simplicité et de sa puissance dans C#.
keywords: C# , Aspose.3D for .NET , The first application using Aspose.3D for .NET, The first program via Aspose.3D for .NET.
---
{{% alert color="primary" %}}

This tutorial explains how to create your first application using Aspose.3D's simple API. This simple application creates a 3d file in a specified 3D scene.

{{% /alert %}}

##  **Comment créer l'application**

Les étapes ci-dessous créent l'application en utilisant Aspose.3D API:

1. Créez une instance de la classe [Scène](https://reference.aspose.com/3d/net/aspose.threed/scene/).
1. Si vous avez une licence, alors [L'appliquer](/3d/fr/net/licensing/).
Si vous utilisez la version d'évaluation, ignorez les lignes de code liées à la licence.
1. Créez un nouveau fichier 3D ou ouvrez un fichier 3D existant.
1. Accédez au contenu de la scène dans le fichier 3D.
1. Générez le fichier 3D modifié.

La mise en œuvre des étapes ci-dessus est démontrée dans les exemples ci-dessous.

###  **Comment créer un nouveau document de scène**

L'exemple suivant crée un nouveau fichier de scène 3D à partir de zéro. Tout d'abord, créez une scène 3D, puis enregistrez le fichier au format FBX.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET

// Create an object of the Scene class
Scene scene = new Scene();
// Save 3D scene document
scene.Save("document.fbx");

{{< /highlight >}}

###  **Comment ouvrir un fichier existant**

L'exemple suivant ouvre un fichier de modèle 3D existant nommé "document.fbx", puis enregistre la scène ou le document 3D dans un flux dans divers formats 3D pris en charge.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
                        
// Load a 3D document into Aspose.3D
Scene scene = new Scene();

// Open an existing 3D scene
scene.Open("document.fbx");

// Save Scene to a stream
MemoryStream dstStream = new MemoryStream();
scene.Save(dstStream, FileFormat.FBX7500ASCII);
            
// Save Scene to a local path
scene.Save("output_out.fbx");

{{< /highlight >}}
