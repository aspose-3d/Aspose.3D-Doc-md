---
title: Упростить создание матрицы преобразования цепными операциями
type: docs
weight: 60
url: /ru/net/simplify-the-creation-of-transformation-matrix-by-the-chain-operations/
description: Aspose.3D for .NET API предлагает класс TransformBuilder, который упрощает создание матрицы преобразования с помощью цепных операций.
---
{{% alert color="primary" %}} 

Aspose.3D for .NET API предлагает класс `TransformBuilder`, который упрощает создание матрицы преобразования цепными операциями.

{{% /alert %}} 

Предположим, есть экземпляр TransformBuilder**Тб**, И цепные операции:

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

Новые добавленные методы в классах `Matrix4` и `TransformBuilder`-это утилиты для разработчиков для моделирования сцены за программой, поэтому им не нужно вручную строить матрицу преобразования, ее обычно используют опытные разработчики.

Порядковые разработчики могут использовать свойство `Transform` класса `Node` для изменения преобразования/масштабирования/вращения объекта.

Разработчики также могут присвоить матрицу, созданную `TransformBuilder`, `Node.Transform`.

Более подробную информацию о матрице трансформации можно найти в Википедии[Матрица трансформации](https://en.wikipedia.org/wiki/Transformation_matrix#Examples_in_3D_computer_graphics)И[Аффинная трансформация](https://en.wikipedia.org/wiki/Affine_transformation)

{{% /alert %}}
