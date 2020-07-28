+++
title = "Simplify the creation of transformation matrix by the chain operations" 
description = "" 
weight = 12028 
+++

Aspose.3D for .NET : Simplify the creation of transformation matrix by the chain operations  

# Aspose.3D for .NET : Simplify the creation of transformation matrix by the chain operations


Aspose.3D for .NET API offers the TransformBuilder class which simplifies the creation of the transformation matrix by the chain operations.

Suppose, there is a TransformBuilder instance **tb**, and chain operations:

**C#**

{{< code lang="c#" >}}
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
{{< /code >}}

If the compose order of this instance is Prepend, the final matrix is calculated from the left to right, that means the final transformation matrix will do these tasks:

1.  Change the (x, y, z) into (x + 1, y, z)
2.  Rotate alone with the Y axis with 180deg will change the (x, y, z) into (-x, y, -z)
3.  Scale by 2 will change the (x, y, z) into (2x, 2y, 2z)
4.  Change the (x, y, z) into (z, y, x)

But if the compose order is Append, the order will be reversed like:

1.  Change the (x, y, z) into (z, y, x)
2.  Scale by 2 will change the (x, y, z) into (2x, 2y, 2z)
3.  Rotate alone with the Y axis with 180deg will change the (x, y, z) into (-x, y, -z)
4.  Change the (x, y, z) into (x + 1, y, z)

**C#**

{{< code lang="c#" >}}
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
{{< /code >}}

The new added methods in the **Matrix4** and **TransformBuilder** classes are the utilities for developers to model the scene by program, so they do not need to manually construct the transform matrix, this is usually used by expert developers.

Ordinal developers can use the **Transform** property of class **Node** to change the translation/scaling/rotation of an object.

Developers can also assign the matrix created by **TransformBuilder** to **Node.Transform**.

More information about transformation matrix can be found at Wikipedia [Transformation matrix](https://en.wikipedia.org/wiki/Transformation_matrix#Examples_in_3D_computer_graphics) and [Affine Transofrmation](https://en.wikipedia.org/wiki/Affine_transformation)

