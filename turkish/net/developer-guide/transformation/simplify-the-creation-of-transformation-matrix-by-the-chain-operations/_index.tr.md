---
title: Szincir işlemleri ile dönüşüm matrisinin oluşturulmasını içerir
type: docs
weight: 60
url: /tr/net/simplify-the-creation-of-transformation-matrix-by-the-chain-operations/
description: Aspose.3D for .NET API, dönüşüm matrisinin zincir işlemleri tarafından oluşturulmasını kolaylaştıran transformbuilder sınıfını sunar.
---
{{% alert color="primary" %}} 

Aspose.3D for .NET API, dönüşüm matrisinin zincir işlemleri tarafından oluşturulmasını kolaylaştıran `TransformBuilder` sınıfını sunar.

{{% /alert %}} 

Suppose, bir Transformuuilder örneği var**Tb**Ve zincir işlemleri:

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

If bu örneğin oluştur sırası Prepend, son matris soldan sağa hesaplanır, bu da son dönüşüm matrisinin bu görevleri yapacağı anlamına gelir:

1. (X, y, z) içine (x 1, y, z)
1. 180180deg ile Y ekseni ile tek başına (x, y, z) (-x, y, -z)
1. Scale 2 ile (x, y, z) (2x, 2y, 2z) olarak değişecek
1. Change (x, y, z) içine (z, y, x)

Compose ut sipariş Append ise, sipariş aşağıdaki gibi tersine çevrilecektir:

1. Change (x, y, z) içine (z, y, x)
1. Scale 2 ile (x, y, z) (2x, 2y, 2z) olarak değişecek
1. 180180deg ile Y ekseni ile tek başına (x, y, z) (-x, y, -z)
1. (X, y, z) içine (x 1, y, z)

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

`Matrix4` ve `TransformBuilder` sınıflarındaki yeni eklenen yöntemler, geliştiricilerin sahneyi programa göre modellemesi için yardımcı programlardır, bu nedenle dönüşüm matrisini manuel olarak oluşturmalarına gerek yoktur, bu genellikle uzman geliştiriciler tarafından kullanılır.

Ordinal developers can use the `Transform` property of class `Node` to change the translation/scaling/rotation of an object.

Developers can also assign the matrix created by `TransformBuilder` to `Node.Transform`.

Dönüşüm matrisi hakkında daha fazla bilgi vikipedi [Transformation matrisi](https://en.wikipedia.org/wiki/Transformation_matrix#Examples_in_3D_computer_graphics) ve [Affine Transofrmation](https://en.wikipedia.org/wiki/Affine_transformation) adresinde bulunabilir.

{{% /alert %}}
