---
title: Créer une scène avec des formes primitives 3D
type: docs
weight: 20
url: /fr/java/create-scene-with-primitive-3d-shapes/
description: Aspose.3D for Java API supporte les formes primitives 3D. Toutes les primitives paramétrées seront converties en maillage automatiquement tout en sauvegardant dans n'importe quel format de fichier de sortie pris en charge.
---
{{% alert color="primary" %}} 

Aspose.3D for Java API supporte les formes primitives 3D. Toutes les primitives paramétrées seront converties en maillage automatiquement tout en sauvegardant dans n'importe quel format de fichier de sortie pris en charge.

{{% /alert %}} 
##  **Construire une scène à partir de formes primitives 3D**
La modélisation est le processus de création pure et Aspose.3D API supporte la création d'une scène avec des formes primitives 3D.
###  **Échantillon de programmation**
Cet exemple de code crée une scène avec des formes primitives 3D et enregistre dans le fichier FBX.

{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// Initialize a Scene object
Scene scene = new Scene();
// Create a Box model
scene.getRootNode().createChildNode("box", new Box());
// Create a Cylinder model
scene.getRootNode().createChildNode("cylinder", new Cylinder());
// Save drawing in the FBX format
MyDir = MyDir + RunExamples.getOutputFilePath("test.fbx");
scene.save(MyDir, FileFormat.FBX7500ASCII);
{{< /highlight >}}
