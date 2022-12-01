---
title: Szincir işlemleri ile dönüşüm matrisinin oluşturulmasını içerir
type: docs
weight: 60
url: /tr/net/simplify-the-creation-of-transformation-matrix-by-the-chain-operations/
description: Aspose.3D for .NET API, dönüşüm matrisinin zincir işlemleri tarafından oluşturulmasını kolaylaştıran TransformBuilder sınıfını sunar.
---
{{% alert color="primary" %}} 

Aspose.3D for .NET API, zincir işlemleri ile dönüşüm matrisinin oluşturulmasını kolaylaştıran `TransformBuilder` sınıfını sunar.

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

07o `Matrix4` ve `TransformBuilder` sınıflarında yeni eklenen yöntemler, geliştiricilerin sahneyi programa göre modellemesi için yardımcı programlardır, bu yüzden dönüşüm matrisini manuel olarak oluşturmalarına gerek yoktur, bu genellikle uzman geliştiriciler tarafından kullanılır.

Dinal r. geliştiricileri, bir nesnenin çeviri/ölçekleme/dönüşünü değiştirmek için `Transform` sınıfı `Node` özelliğini kullanabilir.

Developers ayrıca `TransformBuilder` ile `Node.Transform` arasında oluşturulan matrisi atayabilir.

Dönüşüm matrisi hakkında cevher bilgisi Wikipedia'da bulunabilir[Transformation matrisi](https://en.wikipedia.org/wiki/Transformation_matrix#Examples_in_3D_computer_graphics)Ve[Affine Transofrmation](https://en.wikipedia.org/wiki/Affine_transformation)

{{% /alert %}}
