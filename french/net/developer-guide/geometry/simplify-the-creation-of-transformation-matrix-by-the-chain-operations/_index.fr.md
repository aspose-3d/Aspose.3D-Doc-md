---
title: Simplifier la création de matrice de transformation par les opérations de la chaîne
type: docs
weight: 60
url: /fr/net/simplify-the-creation-of-transformation-matrix-by-the-chain-operations/
description: Aspose.3D for .NET API offre la classe TransformBuilder qui simplifie la création de la matrice de transformation par les opérations en chaîne.
---
{{% alert color="primary" %}} 

Aspose.3D for .NET API propose la classe `TransformBuilder` qui simplifie la création de la matrice de transformation par les opérations en chaîne.

{{% /alert %}} 

Supposons qu'il y ait une instance TransformBuilder**Tb**, Et opérations de chaîne:

**C#**

{{< highlight "java" >}}

 // Change the (x, y, z) into (x + 1, y, z)

var a = tb.Translate(1, 0, 0)

// Rotate alone with the Y axis with 180 deg will change the (x, y, z) into (-x, y, -z)

.RotateEulerDegree(0, 180, 0)

// Scale by 2 will change the (x, y, z) into (2x, 2y, 2z)

.Scale(2)

// change the (x, y, z) into (z, y, x)

.Rearrange(Axis.ZAxis, Axis.YAxis, Axis.XAxis)

.Matrix;



public enum ComposeOrder

{

   /// <summary>

   /// Append the new transform to the chain

   /// </summary>

   Append,

   /// <summary>

   /// Prepend the new transform to the chain

   /// </summary>

   Prepend

}

{{< /highlight >}}

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

**C#**

{{< highlight "java" >}}

 //use prepend order so the calculation is performed from left to right:

var m = (new TransformBuilder(ComposeOrder.Prepend))

   //Change the (x, y, z) into (x + 1, y, z)

   .Translate(1, 0, 0)

   // Rotate alone with the Y axis with 180deg will change the (x, y, z) into (-x, y, -z)

   .RotateEulerDegree(0, 180, 0)

   //Scale by 2 will change the (x, y, z) into (2x, 2y, 2z)

   .Scale(2)

   //change the (x, y, z) into (z, y, x)

   .Rearrange(Axis.ZAxis, Axis.YAxis, Axis.XAxis)

   .Matrix;

 //Apply this matrix on a (0, 0, 0) vector, then we get the right result (0, 0, -2)

 var t = m * Vector3.Origin;

{{< /highlight >}}

{{% alert color="primary" %}} 

Les nouvelles méthodes ajoutées dans les classes `Matrix4` et `TransformBuilder` sont les utilitaires permettant aux développeurs de modéliser la scène par programme, ils n'ont donc pas besoin de construire manuellement la matrice de transformation, cela est généralement utilisé par les développeurs experts.

Les développeurs ordinaux peuvent utiliser la propriété `Transform` de la classe `Node` pour modifier la traduction/mise à l'échelle/rotation d'un objet.

Les développeurs peuvent également attribuer la matrice créée par `TransformBuilder` au `Node.Transform`.

Plus d'informations sur la matrice de transformation peuvent être trouvées sur Wikipedia[Matrice de transformation](https://en.wikipedia.org/wiki/Transformation_matrix#Examples_in_3D_computer_graphics)Et[Affine Transofrmation](https://en.wikipedia.org/wiki/Affine_transformation)

{{% /alert %}}
