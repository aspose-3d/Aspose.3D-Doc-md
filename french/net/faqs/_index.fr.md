---
title: FAQs
type: docs
weight: 190
url: /fr/net/faqs/
description: Foire aux questions sur Aspose.3D pour. Net.
---
####  **Q: Comment animer FBX ou une autre propriété spéciale du format 3D qui n'a pas été définie dans Aspose.3D?**
* A **: Créez une propriété dynamique sur l'objet cible et effectuez une animation de propriété sur la propriété dynamique, car la propriété dépend du format de fichier concret, Aspose.3D ne peut pas garantir que l'animation fonctionne lorsque vous enregistrez la scène dans un autre type de format.
####  **Q: Pourquoi l'animation sur le nœud racine de la scène ne fonctionne pas lorsqu'elle est sérialisée dans le fichier FBX?**
* A **: Le format FBX ne vous permet pas d'accéder aux propriétés du nœud racine, donc l'animation ne fonctionnera pas.
####  **Q: Pourquoi ai-je changé l'information d'actif sur la scène, et essayer d'importer le fichier FBX généré à 3ds max, ces informations ont toutes été perdues?**
* A **: 3Ds MAX ou d'autres logiciels ne peuvent importer que FBX fichier, mais pas ouvrir le FBX fichier, cela signifie qu'il vous permet d'importer plusieurs FBX à l'intérieur d'une scène, si l'information de l'actif peut être appliquée à la scène actuelle, alors vos informations de scène d'origine peuvent être écrasées par l'importation, C'est donc la politique de conception de 3Ds MAX de ne pas importer les informations sur les actifs de la scène.


####  **Q: Un nœud est constitué de plusieurs mailles (pour le verre, le cadre, etc.). Tous ces maillages sont dans la liste d'entités du nœud. Comment ajouter un matériau à tous ces nœuds (le matériau est juste la couleur)?**
* A **: La meilleure solution devrait créer des sous-nœuds pour chaque maillage et assigner un matériau différent à chaque sous-nœud.