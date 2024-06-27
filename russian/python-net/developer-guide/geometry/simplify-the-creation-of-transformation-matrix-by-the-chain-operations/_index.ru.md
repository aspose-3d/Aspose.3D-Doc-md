---
title: Упростить создание матрицы преобразования цепными операциями
type: docs
weight: 60
url: /ru/python-net/simplify-the-creation-of-transformation-matrix-by-the-chain-operations/
description: Aspose.3D for Python via .NET API предлагает класс TransformBuilder, который упрощает создание матрицы преобразования операциями цепочки.
---
{{% alert color="primary" %}} 

Aspose.3D for Python via .NET API предлагает класс `TransformBuilder`, который упрощает создание матрицы преобразования операциями цепочки.

{{% /alert %}} 

Предположим, что есть экземпляр `TransformBuilder`**Тб**, И цепные операции:

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

Если порядок составления этого экземпляра-Prepend, конечная матрица вычисляется слева направо, что означает, что последняя матрица преобразования выполнит эти задачи:

1. Измените (x, y, z) на (x 1, y, z)
1. Поворот отдельно с осью Y с 180deg изменит (x, y, z) на (-x, y, -z)
1. Масштаб на 2 изменит (x, y, z) на (2x, 2y, 2z)
1. Измените (x, y, z) на (z, y, x)

Но если порядок сочинения-Append, порядок будет изменен так:

1. Измените (x, y, z) на (z, y, x)
1. Масштаб на 2 изменит (x, y, z) на (2x, 2y, 2z)
1. Поворот отдельно с осью Y с 180deg изменит (x, y, z) на (-x, y, -z)
1. Измените (x, y, z) на (x 1, y, z)

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

Новые методы в классах `Matrix4` и `TransformBuilder` являются утилитами для разработчиков для моделирования сцены по программе, поэтому им не нужно вручную создавать матрицу преобразования, это обычно используется опытными разработчиками.

Обычные разработчики могут использовать свойство `Transform` класса `Node` для изменения трансляции/масштабирования/вращения объекта.

Разработчики также могут назначить матрицу, созданную `TransformBuilder`, `Node.Transform`.

Более подробную информацию о матрице преобразования можно найти в Википедии [Матрица трансформации](https://en.wikipedia.org/wiki/Transformation_matrix#Examples_in_3D_computer_graphics) и [Аффинная трансформация](https://en.wikipedia.org/wiki/Affine_transformation)

{{% /alert %}}
