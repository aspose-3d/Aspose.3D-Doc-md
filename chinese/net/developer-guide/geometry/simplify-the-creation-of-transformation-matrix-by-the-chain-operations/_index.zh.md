---
title: 通过链式操作简化变换矩阵的创建
type: docs
weight: 60
url: /zh/net/simplify-the-creation-of-transformation-matrix-by-the-chain-operations/
description: Aspose.3D for .NET API提供了TransformBuilder类，它通过链操作简化了转换矩阵的创建。
---
{{% alert color="primary" %}} 

Aspose.3D for .NET API提供了`TransformBuilder`类，它通过链操作简化了变换矩阵的创建。

{{% /alert %}} 

假设，有一个TransformBuilder实例**结核病**,以及连锁经营:

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

如果此实例的合成顺序为Prepend，则从左到右计算最终矩阵，这意味着最终转换矩阵将执行以下任务:

1. 将 (x，y，z) 改为 (x 1，y，z)
1. 以180度的y轴单独旋转会将 (x，Y，z) 变为 (-x，y，-z)
1. 缩放2将把 (x，y，z) 变成 (2x，2y，2z)
1. 将 (x，y，z) 改为 (z，y，x)

但是，如果附加了撰写顺序，则顺序将反转，例如:

1. 将 (x，y，z) 改为 (z，y，x)
1. 缩放2将把 (x，y，z) 变成 (2x，2y，2z)
1. 以180度的y轴单独旋转会将 (x，Y，z) 变为 (-x，y，-z)
1. 将 (x，y，z) 改为 (x 1，y，z)

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

`Matrix4`和`TransformBuilder`类中新添加的方法是开发人员通过程序对场景进行建模的实用工具，因此他们不需要手动构造变换矩阵，这通常由专家开发人员使用。

序数开发人员可以使用类`Node`的`Transform`属性来更改对象的平移/缩放/旋转。

开发人员还可以将`TransformBuilder`创建的矩阵分配给`Node.Transform`。

更多关于变换矩阵的信息可以在维基百科找到[变换矩阵](https://en.wikipedia.org/wiki/Transformation_matrix#Examples_in_3D_computer_graphics)和[仿射传输](https://en.wikipedia.org/wiki/Affine_transformation)

{{% /alert %}}
