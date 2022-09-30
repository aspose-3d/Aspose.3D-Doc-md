---
title: FAQ
type: docs
weight: 190
url: /fr/net/faqs/
description: Foire aux questions sur Aspose.3D pour. Net.
---
#### **Q: Comment animer FBX ou la propriété spéciale d'un autre format 3D qui n'a pas été définie dans Aspose.3D?**
** A **: Créez une propriété dynamique sur l'objet cible et effectuez une animation de propriété sur la propriété dynamique, car la propriété dépend du format de fichier concret, Aspose.3D ne peut pas garantir que l'animation peut fonctionner lorsque vous enregistrez la scène dans un autre type de format.
#### **Q: Pourquoi l'animation sur le nœud racine de la scène ne fonctionne-t-elle pas lorsqu'elle est sérialisée dans le fichier FBX?**
** A **: Le format FBX ne vous permet pas d'accéder aux propriétés du nœud racine, donc l'animation ne fonctionnera pas.
#### **Q: Pourquoi j'ai changé les informations sur les ressources sur la scène et essayer d'importer le fichier FBX généré à 3ds max, ces informations ont toutes été perdues?**
** A **: 3Ds MAX ou certains autres logiciels ne peuvent importer que le fichier FBX, mais n'ouvrent pas le fichier FBX, ce qui signifie qu'il vous permet d'importer plusieurs FBX dans une scène, si les informations de l'actif peuvent être appliquées à la scène actuelle, alors vos informations de scène d'origine peuvent être écrasées par importation, C'est donc la politique de conception de 3Ds MAX de ne pas importer les informations sur les actifs de la scène.
