---
title: Créer un document 3D vide
type: docs
weight: 20
url: /fr/java/create-an-empty-3d-document/
description: Aspose.3D for Java API supporte la création d'une scène 3D à partir de zéro, puis sauvegarde au format 3D pris en charge.
---
##  **Créez une scène vide 3D et enregistrez au format 3D pris en charge**
Aspose.3D for Java API supporte la création d'une scène 3D à partir de zéro, puis sauvegarde au format 3D pris en charge.
###  **Création d'une scène 3D vide**
Veuillez suivre ces étapes pour créer une scène 3D avec Aspose.3D for Java API:

1. Créer une instance de l'**Scène**Qui représente 3D scène.
1. Générez le document 3D en appelant le**Sauver**Méthode de la**Scène**Instance de classe.
####  **Création d'une scène 3D vide: échantillons de programmation**
{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
MyDir = MyDir + "document.fbx";
// Create an object of the Scene class
Scene scene = new Scene();
// Save 3D scene document
scene.save(MyDir, FileFormat.FBX7500ASCII);
{{< /highlight >}}




