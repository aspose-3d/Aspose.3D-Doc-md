---
title: Générer des données normales pour tous les mailles du modèle 3D
type: docs
weight: 40
url: /fr/java/generate-normal-data-for-all-meshes-of-3d-model/
description: Aspose.3D for Java API a l'appui de la génération de données normales pour tous les mailles du modèle 3D (sans les données normales).
---
{{% alert color="primary" %}} 

Aspose.3D for Java API a l'appui de la génération de données normales pour tous les mailles du modèle 3D (sans les données normales).

{{% /alert %}} 
## **Générer des données normales pour tous les mailles du modèle 3DS**
La méthode générateNormal exposée par la classe `PolygonModifier` peut être utilisée pour générer des données normales pour tous les maillages d'un fichier 3DS. Si l'élément VertexElementSmoothingGroup a été défini dans le maillage, les données normales générées seront lissées par le VertexElementSmoothingGroup.
### **Échantillon de programmation**
Cet exemple de code charge un fichier 3DS, visitez tous les nœuds et créez des données normales pour tous les maillages.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-objects-GenerateDataForMeshes.java" >}}
