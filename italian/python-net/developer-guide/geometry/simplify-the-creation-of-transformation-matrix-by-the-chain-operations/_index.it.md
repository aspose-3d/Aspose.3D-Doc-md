---
title: Semplificare la creazione della matrice di trasformazione dalle operazioni della catena
type: docs
weight: 60
url: /it/python-net/simplify-the-creation-of-transformation-matrix-by-the-chain-operations/
description: Aspose.3D for Python via .NET API offre la classe TransformBuilder che semplifica la creazione della matrice di trasformazione in base alle operazioni della catena.
---
{{% alert color="primary" %}} 

Aspose.3D for Python via .NET API offre la classe `TransformBuilder` che semplifica la creazione della matrice di trasformazione in base alle operazioni della catena.

{{% /alert %}} 

Supponiamo che ci sia un'istanza di `TransformBuilder`**Tb**E operazioni a catena:

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

Se l'ordine di composizione di questa istanza è Prepenend, la matrice finale viene calcolata da sinistra a destra, ciò significa che la matrice di trasformazione finale farà queste attività:

1. Cambia il (x, y, z) in (x 1, y, z)
1. Ruotare da solo con l'asse Y con 180gradi cambierà (x, y, z) in (-x, y, -z)
1. La scala di 2 cambierà (x, y, z) in (2x, 2y, 2z)
1. Cambia il (x, y, z) in (z, y, x)

Ma se l'ordine di composizione è Appendi, l'ordine verrà invertito come:

1. Cambia il (x, y, z) in (z, y, x)
1. La scala di 2 cambierà (x, y, z) in (2x, 2y, 2z)
1. Ruotare da solo con l'asse Y con 180gradi cambierà (x, y, z) in (-x, y, -z)
1. Cambia il (x, y, z) in (x 1, y, z)

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

I nuovi metodi aggiunti nelle classi `Matrix4` e `TransformBuilder` sono le utilità per gli sviluppatori per modellare la scena per programma, quindi non è necessario costruire manualmente la matrice di trasformazione, di solito viene utilizzata da sviluppatori esperti.

Gli sviluppatori ordinali possono utilizzare la proprietà `Transform` della classe `Node` per modificare la traduzione/ridimensionamento/rotazione di un oggetto.

Gli sviluppatori possono anche assegnare la matrice creata da `TransformBuilder` a `Node.Transform`.

Ulteriori informazioni sulla matrice di trasformazione sono disponibili su Wikipedia [Matrice di trasformazione](https://en.wikipedia.org/wiki/Transformation_matrix#Examples_in_3D_computer_graphics) e [Transofrmation affine](https://en.wikipedia.org/wiki/Affine_transformation)

{{% /alert %}}
