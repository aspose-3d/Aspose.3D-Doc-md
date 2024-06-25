---
title: Arbeiten mit Zylinder
type: docs
weight: 130
url: /de/net/working-with-cylinder/
description: Aspose.3D for .NET ermöglicht das Anpassen von Offset-Oberteil eines Zylinders. Um diese Funktional ität zu nutzen, können Sie die Offset-Eigenschaft der Cylinder-Klasse verwenden.
---
#  **Offset-Top anpassen**
Aspose.3D for .NET ermöglicht das Anpassen von Offset-Oberteil eines Zylinders. Um diese Funktional ität nutzen zu können, können Sie die Eigenschaft `Offset` der `Cylinder`-Klasse verwenden. Das folgende Code-Snippet zeigt, wie Offset Top angepasst wird:



{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-WorkingWithCylinder-CustomizedOffsetTopCylinder-1.cs" >}}

! [Todo: image_alt_text](working-with-cylinder_1.png)

Im linken ist OffsetTop auf (5, 3, 0) eingestellt. Es ist leicht zu erkennen, dass sich die obere Kappe bewegt hat und auch der gesamte Torso betroffen ist.
#  **Shear Bottom anpassen**
Aspose.3D for .NET ermöglicht die Anpassung des Scher bodens eines Zylinders. Um diese Funktional ität nutzen zu können, können Sie die Eigenschaft `ShearBottom` der `Cylinder`-Klasse verwenden. Das folgende Code-Snippet zeigt, wie Shear Bottom angepasst wird:



{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-WorkingWithCylinder-CustomizedShearBottomCylinder-1.cs" >}}

! [Todo: image_alt_text](working-with-cylinder_2.png)

Der linke Zylinder hat `ShearBottom` bis (0, 0.83), während der rechte ein Ordnungszylinder ist.
#  **Lüfter zylinder erstellen**
Aspose.3D for .NET ermöglicht die Erstellung eines Lüfter zylinders. Um diese Funktional ität nutzen zu können, können Sie die Eigenschaft `GenerateFanCylinder` der Klasse `Cylinder` auf `true` festlegen. Das folgende Code-Snippet zeigt, wie diese Funktional ität verwendet wird:



{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-WorkingWithCylinder-CustomizedShearBottomCylinder-1.cs" >}}

! [Todo: image_alt_text](working-with-cylinder_3.png)

Der linke Zylinder hat `GenerateFanCylinder = false` und der rechte hat `GenerateFanCylinder = true`.
