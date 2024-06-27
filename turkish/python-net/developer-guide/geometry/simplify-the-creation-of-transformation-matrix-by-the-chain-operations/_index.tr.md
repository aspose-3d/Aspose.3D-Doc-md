---
title: Szincir işlemleri ile dönüşüm matrisinin oluşturulmasını içerir
type: docs
weight: 60
url: /tr/python-net/simplify-the-creation-of-transformation-matrix-by-the-chain-operations/
description: Aspose.3D for Python via .NET API, dönüşüm matrisinin zincir işlemleri tarafından oluşturulmasını kolaylaştıran transformbuilder sınıfını sunar.
---
{{% alert color="primary" %}} 

Aspose.3D for Python via .NET API, dönüşüm matrisinin zincir işlemleri tarafından oluşturulmasını kolaylaştıran `TransformBuilder` sınıfını sunar.

{{% /alert %}} 

Varsayalım, bir `TransformBuilder` örneği var**Tb**Ve zincir işlemleri:

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

`Matrix4` ve `TransformBuilder` sınıflarındaki yeni eklenen yöntemler, geliştiricilerin sahneyi programa göre modellemesi için yardımcı programlardır, bu nedenle dönüşüm matrisini manuel olarak oluşturmalarına gerek yoktur, bu genellikle uzman geliştiriciler tarafından kullanılır.

Ordinal developers can use the `Transform` property of class `Node` to change the translation/scaling/rotation of an object.

Developers can also assign the matrix created by `TransformBuilder` to `Node.Transform`.

Dönüşüm matrisi hakkında daha fazla bilgi vikipedi [Transformation matrisi](https://en.wikipedia.org/wiki/Transformation_matrix#Examples_in_3D_computer_graphics) ve [Affine Transofrmation](https://en.wikipedia.org/wiki/Affine_transformation) adresinde bulunabilir.

{{% /alert %}}
