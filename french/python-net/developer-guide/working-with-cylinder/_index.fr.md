---
title: Travailler avec le cylindre
type: docs
weight: 130
url: /fr/python-net/working-with-cylinder/
description: Aspose.3D pour Python via .NET permet de personnaliser le haut offset d'un cylindre. Pour utiliser cette fonctionnalité, vous pouvez utiliser la propriété Offset de la classe Cylindre.
---
# **Personnaliser le haut offset**
Aspose.3D pour Python via .NET permet de personnaliser le haut offset d'un cylindre. Afin d'utiliser cette fonctionnalité, vous pouvez utiliser `offset` propriété de `Cylinder` classe. L'extrait de code suivant montre comment personnaliser Offset Top:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithCylinder-CustomizedOffsetTopCylinder-1.py" >}}

![Todo: image_Alt_Texte](working-with-cylinder_1.png)

Celui de gauche a `offset_top` réglé sur (5, 3, 0), il est facile de voir que le capuchon supérieur a bougé et que tout le torse est également affecté.
# **Personnaliser ShearBottom**
Aspose.3D pour Python via .NET permet de personnaliser le fond de cisaillement d'un cylindre. Afin d'utiliser cette fonctionnalité, vous pouvez utiliser `shear_bottom` propriété de `Cylinder` classe. L'extrait de code suivant montre comment personnaliser le fond de cisaillement:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithCylinder-CustomizedShearBottomCylinder-1.py" >}}

![Todo: image_Alt_Texte](working-with-cylinder_2.png)

Le cylindre gauche a `shear_bottom` à (0, 0,83) tandis que celui de droite est un cylindre ordinal.
# **Créer un ventilateur-cylindre**
Aspose.3D pour Python via .NET permet de créer un cylindre de ventilateur. Afin d'utiliser cette fonctionnalité, vous pouvez définir la propriété `generate_fan_cylinder` de la classe `Cylinder` à `True`. L'extrait de code suivant montre comment utiliser cette fonctionnalité:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithCylinder-CustomizedShearBottomCylinder-1.py" >}}

![Todo: image_Alt_Texte](working-with-cylinder_3.png)

Le cylindre gauche a `generate_fan_cylinder = False` et celui de droite a `generate_fan_cylinder = True`.
