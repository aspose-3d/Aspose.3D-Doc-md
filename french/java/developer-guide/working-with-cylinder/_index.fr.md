---
title: Travailler avec le cylindre
type: docs
weight: 100
url: /fr/java/working-with-cylinder/
description: Aspose.3D for Java permet de personnaliser le haut décalé d'un cylindre. Pour utiliser cette fonctionnalité, vous pouvez utiliser la méthode setOffsetTop() de la classe Cylinder.
---
#  **Personnaliser le haut offset**
Aspose.3D for Java permet de personnaliser le haut décalé d'un cylindre. Pour utiliser cette fonctionnalité, vous pouvez utiliser la méthode `setOffsetTop()` de la classe `Cylinder`. L'extrait de code suivant montre comment personnaliser Offset Top:



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "CustomizedOffsetTopCylinder.java" >}}

! [Tout le monde: image_alt_text](working-with-cylinder_1.png)

Celui de gauche a OffsetTop réglé sur (5, 3, 0), il est facile de voir que la casquette supérieure a bougé et que tout le torse est également affecté.
#  **Personnaliser ShearBottom**
Aspose.3D for Java permet de personnaliser le fond de cisaillement d'un cylindre. Pour utiliser cette fonctionnalité, vous pouvez utiliser la propriété `setShearBottom()` de la classe `Cylinder`. L'extrait de code suivant montre comment personnaliser Shear Bottom:



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "CustomizedShearBottomCylinder.java" >}}

! [Tout le monde: image_alt_text](working-with-cylinder_2.png)

Le cylindre gauche a ShearBottom à (0, 0,83) tandis que celui de droite est un cylindre ordinal.
#  **Créer un ventilateur-cylindre**
Aspose.3D for Java permet de créer un cylindre de ventilateur. Pour utiliser cette fonctionnalité, vous pouvez utiliser la propriété `setGenerateFanCylinder()` de la classe `Cylinder` à `true`. L'extrait de code suivant montre comment utiliser cette fonctionnalité:



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "CreateFanCylinder.java" >}}

! [Tout le monde: image_alt_text](working-with-cylinder_3.png)

Le cylindre gauche a GenerateFanCylinder = faux et celui de droite a GenerateFanCylinder = true.
