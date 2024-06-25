---
title: Simplifier la création de matrice de transformation par les opérations de la chaîne
type: docs
weight: 60
url: /fr/python-net/simplify-the-creation-of-transformation-matrix-by-the-chain-operations/
description: Aspose.3D for Python via .NET API offre la classe TransformBuilder qui simplifie la création de la matrice de transformation par les opérations de la chaîne.
---
{{% alert color="primary" %}} 

Aspose.3D for Python via .NET API offre la classe `TransformBuilder` qui simplifie la création de la matrice de transformation par les opérations de la chaîne.

{{% /alert %}} 

Supposons qu'il existe une instance `TransformBuilder`**Tb**, Et opérations de chaîne:

**Python**

```py

import aspose.threed as a3d

# Change the (x, y, z) into (x + 1, y, z)

tb = a3d.utilities.TransformBuilder(a3d.utilities.ComposeOrder.APPEND)

a = tb.translate(1, 0, 0)
# Rotate alone with the Y axis with 180 deg will change the (x, y, z) into (-x, y, -z)
.rotate_euler_degree(0, 180, 0)
# Scale by 2 will change the (x, y, z) into (2x, 2y, 2z)
.scale(2)
# change the (x, y, z) into (z, y, x)
.rearrange(a3d.Axis.Z_AXIS, a3d.Axis.Y_AXIS, a3d.Axis.X_AXIS)
.matrix


```

Si l'ordre de composition de cette instance est Prependt, la matrice finale est calculée de gauche à droite, cela signifie que la matrice de transformation finale fera ces tâches:

1. Changez le (x, y, z) en (x 1, y, z)
1. Tourner seul avec l'axe Y avec 180 ° g changera le (x, y, z) en (-x, y, -z)
1. L'échelle de 2 changera le (x, y, z) en (2x, 2y, 2z)
1. Changez le (x, y, z) en (z, y, x)

Mais si l'ordre de composition est Append, l'ordre sera inversé comme:

1. Changez le (x, y, z) en (z, y, x)
1. L'échelle de 2 changera le (x, y, z) en (2x, 2y, 2z)
1. Tourner seul avec l'axe Y avec 180 ° g changera le (x, y, z) en (-x, y, -z)
1. Changez le (x, y, z) en (x 1, y, z)

**Python**

```py

import aspose.threed as a3d

# use prepend order so the calculation is performed from left to right:
m = (a3d.utilities.TransformBuilder(a3d.utilities.ComposeOrder.PREPEND))
   # Change the (x, y, z) into (x + 1, y, z)
   .translate(1, 0, 0)
   # Rotate alone with the Y axis with 180deg will change the (x, y, z) into (-x, y, -z)
   .rotate_euler_degree(0, 180, 0)
   # Scale by 2 will change the (x, y, z) into (2x, 2y, 2z)
   .scale(2)
   # change the (x, y, z) into (z, y, x)
   .rearrange(a3d.Axis.Z_AXIS, a3d.Axis.Y_AXIS, a3d.Axis.X_AXIS)
   .matrix
# Apply this matrix on a (0, 0, 0) vector, then we get the right result (0, 0, -2)
 t = m * a3d.utilities.Vector3.ORIGIN;

```

{{% alert color="primary" %}} 

Les nouvelles méthodes ajoutées dans les classes `Matrix4` et `TransformBuilder` sont les utilitaires permettant aux développeurs de modéliser la scène par programme, ils n'ont donc pas besoin de construire manuellement la matrice de transformation, celle-ci est généralement utilisée par les développeurs experts.

Les développeurs ordinaux peuvent utiliser la propriété `Transform` de la classe `Node` pour modifier la traduction/mise à l'échelle/rotation d'un objet.

Les développeurs peuvent également affecter la matrice créée par `TransformBuilder` à `Node.Transform`.

Vous trouverez plus d'informations sur la matrice de transformation sur Wikipedia [Matrice de transformation](https://en.wikipedia.org/wiki/Transformation_matrix#Examples_in_3D_computer_graphics) et [Affine Transofrmation](https://en.wikipedia.org/wiki/Affine_transformation)

{{% /alert %}}
