---
title: Votre première application Aspose.3D
type: docs
weight: 30
url: /fr/python-net/your-first-aspose-3d-application/
---

{{% alert color="primary" %}}

Ce tutoriel explique comment créer votre première application en utilisant l'API simple d'Aspose.3D. Cette application simple crée un fichier 3D dans une scène 3D spécifiée.

{{% /alert %}}

## **Comment créer l'application**

Les étapes suivantes permettent de créer l'application à l'aide de l'API Aspose.3D :

1. Créer une instance de la classe [Scene](https://reference.aspose.com/3d/fr/python-net/aspose.threed/scene/).
1. Si vous avez une licence, alors [appliquez-la](/3d/fr/python-net/licensing/).
   Si vous utilisez la version d'évaluation, ignorez les lignes de code relatives à la licence.
1. Créer un nouveau fichier 3D ou ouvrir un fichier 3D existant.
1. Accéder au contenu de la scène dans le fichier 3D.
1. Générer le fichier 3D modifié.

L'implémentation des étapes ci-dessus est démontrée dans les exemples suivants.

### **Comment créer un document de scène nouveau**

L'exemple suivant crée un nouveau fichier de scène 3D à partir de zéro. Tout d'abord, créez une scène 3D, puis enregistrez le fichier au format FBX.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-CreateEmpty3DDocument.py" >}}

### **Comment ouvrir un fichier existant**

L'exemple suivant ouvre un fichier modèle 3D existant nommé "document.fbx".

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-ReadExistingScene.py" >}}
