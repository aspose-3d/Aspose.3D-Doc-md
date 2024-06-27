---
title: Vereinfachen Sie die Erstellung der Transformation matrix durch die Ketten operationen
type: docs
weight: 60
url: /de/net/simplify-the-creation-of-transformation-matrix-by-the-chain-operations/
description: Aspose.3D for .NET API bietet die TransformBuilder-Klasse, die die Erstellung der Transformation matrix durch die Ketten operationen vereinfacht.
---
{{% alert color="primary" %}} 

Aspose.3D for .NET API bietet die `TransformBuilder`-Klasse, die die Erstellung der Transformation matrix durch die Ketten operationen vereinfacht.

{{% /alert %}} 

Angenommen, es gibt eine TransformBuilder-Instanz**Tb**Und Ketten operationen:

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

Wenn die Kompose-Reihenfolge dieser Instanz Prepend ist, wird die endgültige Matrix von links nach rechts berechnet, was bedeutet, dass die endgültige Transformation matrix diese Aufgaben erledigt:

1. Ändern Sie die (x, y, z) in (x 1, y, z)
1. Drehen Sie sich allein mit der Y-Achse mit 180deg ändert die (x, y, z) in (-x, y, -z)
1. Die Skalierung um 2 ändert die (x, y, z) in (2x, 2y, 2z)
1. Ändern Sie die (x, y, z) in (z, y, x)

Aber wenn die Zusammensetzung reihenfolge Append ist, wird die Reihenfolge wie folgt umgekehrt:

1. Ändern Sie die (x, y, z) in (z, y, x)
1. Die Skalierung um 2 ändert die (x, y, z) in (2x, 2y, 2z)
1. Drehen Sie sich allein mit der Y-Achse mit 180deg ändert die (x, y, z) in (-x, y, -z)
1. Ändern Sie die (x, y, z) in (x 1, y, z)

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

Die neu hinzugefügten Methoden in den Klassen `Matrix4` und `TransformBuilder` sind die Dienst programme für Entwickler, um die Szene nach dem Programm zu modellieren, sodass sie die Transformation matrix nicht manuell erstellen müssen. Dies wird normaler weise von erfahrenen Entwicklern verwendet.

Ordinal-Entwickler können die `Transform`-Eigenschaft der Klasse `Node` verwenden, um die Übersetzung/Skalierung/Rotation eines Objekts zu ändern.

Entwickler können die von `TransformBuilder` erstellte Matrix auch `Node.Transform` zuweisen.

Weitere Informationen zur Transformation matrix finden Sie unter Wikipedia [Transformation matrix](https://en.wikipedia.org/wiki/Transformation_matrix#Examples_in_3D_computer_graphics) und [Affine Trans ofrmation](https://en.wikipedia.org/wiki/Affine_transformation)

{{% /alert %}}
