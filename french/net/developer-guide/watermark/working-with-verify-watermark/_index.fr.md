---
title: Travailler avec la Vérification du Filigrane
type: docs
weight: 170
url: /fr/net/working-with-verify-watermark/
---

{{% alert color="primary" %}}

En utilisant l'API Aspose.3D pour .NET, les développeurs peuvent facilement ajouter une vérification de filigrane aveugle aux fichiers 3D tout en les enregistrant dans n'importe quel format de fichier de sortie pris en charge.

{{% /alert %}}
# **Créer une scène 3D**
Tout d'abord, vous devez créer une scène 3D à partir d'un fichier 3D. Le code ci-dessous montre comment utiliser cette fonctionnalité :

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-WorkingWithWatermark-Create3DScene.cs" >}}

# **Décodez le filigrane**
Aspose.3D pour .NET utilise la méthode `DecodeWatermark` pour confirmer le filigrane du fichier 3D après avoir rempli le mot de passe. Le code ci-dessous montre comment utiliser cette fonctionnalité :

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-WorkingWithVerifyWatermark-DecodeWatermark.cs" >}}

# **Confirmation du document**
Pour le résultat renvoyé, si le résultat renvoyé est nul, cela signifie qu'aucun filigrane n'a été ajouté au document 3D. Si le texte est renvoyé, il s'agit du filigrane du fichier 3D. Si le mot de passe est entré incorrectement, un message d'erreur sera renvoyé.