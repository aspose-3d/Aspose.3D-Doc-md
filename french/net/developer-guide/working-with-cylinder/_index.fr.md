---
title: Travailler avec le cylindre
type: docs
weight: 130
url: /fr/net/working-with-cylinder/
description: Aspose.3D for .NET permet de personnaliser le haut offset d'un cylindre. Pour utiliser cette fonctionnalité, vous pouvez utiliser la propriété Offset de la classe Cylindre.
---
# **Personnaliser le haut offset**
Aspose.3D for .NET permet de personnaliser le haut offset d'un cylindre. Afin d'utiliser cette fonctionnalité, vous pouvez utiliser `Offset` propriété de `Cylinder` classe. L'extrait de code suivant montre comment personnaliser Offset Top:



{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-WorkingWithCylinder-CustomizedOffsetTopCylinder-1.cs" >}}

![Todo: image_Alt_Texte](working-with-cylinder_1.png)

Celui de gauche a OffsetTop réglé sur (5, 3, 0), il est facile de voir que la casquette supérieure a bougé et que tout le torse est également affecté.
# **Personnaliser ShearBottom**
Aspose.3D for .NET permet de personnaliser le fond de cisaillement d'un cylindre. Afin d'utiliser cette fonctionnalité, vous pouvez utiliser `ShearBottom` propriété de `Cylinder` classe. L'extrait de code suivant montre comment personnaliser le fond de cisaillement:



{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-WorkingWithCylinder-CustomizedShearBottomCylinder-1.cs" >}}

![Todo: image_Alt_Texte](working-with-cylinder_2.png)

Le cylindre gauche a `ShearBottom` à (0, 0,83) tandis que celui de droite est un cylindre ordinal.
# **Créer un ventilateur-cylindre**
Aspose.3D for .NET permet de créer un cylindre de ventilateur. Afin d'utiliser cette fonctionnalité, vous pouvez définir la propriété `GenerateFanCylinder` de la classe `Cylinder` à `true`. L'extrait de code suivant montre comment utiliser cette fonctionnalité:



{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-WorkingWithCylinder-CustomizedShearBottomCylinder-1.cs" >}}

![Todo: image_Alt_Texte](working-with-cylinder_3.png)

Le cylindre gauche a `GenerateFanCylinder = false` et celui de droite a `GenerateFanCylinder = true`.
