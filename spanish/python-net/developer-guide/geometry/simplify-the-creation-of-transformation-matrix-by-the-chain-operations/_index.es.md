---
title: Simplificar la creación de la matriz de transformación por las operaciones de la cadena
type: docs
weight: 60
url: /es/python-net/simplify-the-creation-of-transformation-matrix-by-the-chain-operations/
description: Aspose.3D para Python via .NET API ofrece la clase TransformBuilder que simplifica la creación de la matriz de transformación por las operaciones de la cadena.
---
{{% alert color="primary" %}} 

Aspose.3D para Python via .NET API ofrece la clase `TransformBuilder` que simplifica la creación de la matriz de transformación por las operaciones de la cadena.

{{% /alert %}} 

Supongamos que hay una instancia `TransformBuilder`**Tb**, Y operaciones de la cadena:

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

Si el orden de composición de esta instancia es Prepend, la matriz final se calcula de izquierda a derecha, lo que significa que la matriz de transformación final realizará estas tareas:

1. Change (x y z) en (x 1 y z)
1. Girar solo con el eje Y con 180 grados cambiará el (x, y, z) en (-x, y, -z)
1. La escala por 2 cambiará (x, y, z) en (2x, 2y, 2z)
1. Change (x y z) en (z y x)

Pero si el pedido de composición es Append, el pedido se invertirá como:

1. Change (x y z) en (z y x)
1. La escala por 2 cambiará (x, y, z) en (2x, 2y, 2z)
1. Girar solo con el eje Y con 180 grados cambiará el (x, y, z) en (-x, y, -z)
1. Change (x y z) en (x 1 y z)

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

Los nuevos métodos agregados en las clases `Matrix4` y `TransformBuilder` son las utilidades para que los desarrolladores modelen la escena por programa, por lo que no necesitan construir manualmente la matriz de transformación, esto generalmente lo usan desarrolladores expertos.

Los desarrolladores ordinales pueden usar la propiedad `Transform` de la clase `Node` para cambiar la traducción/escalado/rotación de un objeto.

Los desarrolladores también pueden asignar la matriz creada por `TransformBuilder` al `Node.Transform`.

Puede encontrar más información sobre la matriz de transformación en Wikipedia[Matriz de transformación](https://en.wikipedia.org/wiki/Transformation_matrix#Examples_in_3D_computer_graphics)Y[Transofrmación afín](https://en.wikipedia.org/wiki/Affine_transformation)

{{% /alert %}}
