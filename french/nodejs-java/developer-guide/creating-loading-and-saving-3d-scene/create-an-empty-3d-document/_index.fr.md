---
title: Créer un document 3D vide
type: docs
weight: 20
url: /fr/nodejs-java/create-an-empty-3d-document/
description: Aspose.3D for Node.js via Java API supporte la création d'une scène 3D à partir de zéro, puis sauvegarde au format 3D pris en charge.
---
##  **Créez une scène vide 3D et enregistrez au format 3D pris en charge**
Aspose.3D for Node.js via Java API supporte la création d'une scène 3D à partir de zéro, puis sauvegarde au format 3D pris en charge.
###  **Création d'une scène 3D vide**
Veuillez suivre ces étapes pour créer une scène 3D avec Aspose.3D for Node.js via Java API:

1. Créer une instance de l'**Scène**Qui représente 3D scène.
1. Générez le document 3D en appelant le**Sauver**Méthode de la**Scène**Instance de classe.
####  **Création d'une scène 3D vide: échantillons de programmation**
{{< highlight "java" >}}

var file="document.fbx";

// Create an object of the Scene class
var scene = new aspose.threed.Scene();

// Save 3D scene document
scene.save(file);

{{< /highlight >}}




