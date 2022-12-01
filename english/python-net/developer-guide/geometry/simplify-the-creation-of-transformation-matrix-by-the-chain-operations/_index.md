---
title: Simplify the creation of transformation matrix by the chain operations
type: docs
weight: 60
url: /python-net/simplify-the-creation-of-transformation-matrix-by-the-chain-operations/
description: Aspose.3D for Python via .NET API offers the TransformBuilder class which simplifies the creation of the transformation matrix by the chain operations.
---

{{% alert color="primary" %}} 

Aspose.3D for Python via .NET API offers the `TransformBuilder` class which simplifies the creation of the transformation matrix by the chain operations.

{{% /alert %}} 

Suppose, there is a `TransformBuilder` instance **tb**, and chain operations:

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

If the compose order of this instance is Prepend, the final matrix is calculated from the left to right, that means the final transformation matrix will do these tasks:

1. Change the (x, y, z) into (x + 1, y, z)
1. Rotate alone with the Y axis with 180deg will change the (x, y, z) into (-x, y, -z)
1. Scale by 2 will change the (x, y, z) into (2x, 2y, 2z)
1. Change the (x, y, z) into (z, y, x)

But if the compose order is Append, the order will be reversed like:

1. Change the (x, y, z) into (z, y, x)
1. Scale by 2 will change the (x, y, z) into (2x, 2y, 2z)
1. Rotate alone with the Y axis with 180deg will change the (x, y, z) into (-x, y, -z)
1. Change the (x, y, z) into (x + 1, y, z)

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

The new added methods in the `Matrix4` and `TransformBuilder` classes are the utilities for developers to model the scene by program, so they do not need to manually construct the transform matrix, this is usually used by expert developers. 

Ordinal developers can use the `Transform` property of class `Node` to change the translation/scaling/rotation of an object.

Developers can also assign the matrix created by `TransformBuilder` to `Node.Transform`.

More information about transformation matrix can be found at Wikipedia [Transformation matrix](https://en.wikipedia.org/wiki/Transformation_matrix#Examples_in_3D_computer_graphics) and [Affine Transofrmation](https://en.wikipedia.org/wiki/Affine_transformation)

{{% /alert %}}
