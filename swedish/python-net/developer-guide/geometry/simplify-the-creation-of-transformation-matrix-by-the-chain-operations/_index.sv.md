---
title: Förenkla skapandet av transformationsmatris med kedjans åtgärder
type: docs
weight: 60
url: /sv/python-net/simplify-the-creation-of-transformation-matrix-by-the-chain-operations/
description: Aspose.3D for Python via .NET API erbjuder Transformbuilder- klassen som förenklar skapandet av transformationsmatrisen med kedjan.
---
{{% alert color="primary" %}} 

Aspose.3D for Python via .NET API erbjuder klassen `TransformBuilder` som förenklar skapandet av transformationsmatrisen med kedjan.

{{% /alert %}} 

Antag att det finns en `TransformBuilder` instans**Tb**, Och kedjans verksamhet:

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

Om sammansättningsordningen för denna instans är Prepend, beräknas den slutliga matrisen från vänster till höger, Det betyder att den slutliga transformationsmatrisen kommer att utföra dessa uppgifter:

1. Ändra (x, y, z) till (x 1, y, z)
1. Rotera ensam med Y-axeln med 180deg kommer att ändra (x, y, z) till (-x, y, -z)
1. Skala med 2 ändrar (x, y, z) till (2x, 2y, 2z)
1. Ändra (x, y, z) till (z, y, x)

Men om komponera ordern är Tillägg, kommer ordern att vändas som:

1. Ändra (x, y, z) till (z, y, x)
1. Skala med 2 ändrar (x, y, z) till (2x, 2y, 2z)
1. Rotera ensam med Y-axeln med 180deg kommer att ändra (x, y, z) till (-x, y, -z)
1. Ändra (x, y, z) till (x 1, y, z)

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

De nya metoderna i klasserna `Matrix4` och `TransformBuilder` är verktyg för utvecklare att modellera scenen genom program, så de behöver inte manuellt konstruera transforma matrisen, detta brukar användas av expertutvecklare.

Vanliga utvecklare kan använda egenskapen `Transform` för klassen `Node` för att ändra översättning/skalning/rotation av ett objekt.

Utvecklare kan också tilldela matrisen skapad av `TransformBuilder` till `Node.Transform`.

Mer information om transformationsmatris finns på Wikipedia [Transformationsmatris](https://en.wikipedia.org/wiki/Transformation_matrix#Examples_in_3D_computer_graphics) och [Affin överföring](https://en.wikipedia.org/wiki/Affine_transformation)

{{% /alert %}}
