---
title: Arbeiten mit Zylinder
type: docs
weight: 130
url: /de/python-net/working-with-cylinder/
description: Aspose.3D for Python via .NET ermöglicht das Anpassen von Offset Top eines Zylinders. Um diese Funktional ität zu nutzen, können Sie die Offset-Eigenschaft der Cylinder-Klasse verwenden.
---
#  **Offset-Top anpassen**
Aspose.3D for Python via .NET ermöglicht das Anpassen von Offset Top eines Zylinders. Um diese Funktional ität nutzen zu können, können Sie die Eigenschaft `offset` der `Cylinder`-Klasse verwenden. Das folgende Code-Snippet zeigt, wie Offset Top angepasst wird:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithCylinder-CustomizedOffsetTopCylinder-1.py" >}}

! [Todo: image_alt_text](working-with-cylinder_1.png)

Der linke hat `offset_top` auf (5, 3, 0). Es ist leicht zu sehen, dass sich die obere Kappe bewegt hat und auch der gesamte Torso betroffen ist.
#  **Shear Bottom anpassen**
Aspose.3D for Python via .NET ermöglicht die Anpassung des Scher bodens eines Zylinders. Um diese Funktional ität nutzen zu können, können Sie die Eigenschaft `shear_bottom` der `Cylinder`-Klasse verwenden. Das folgende Code-Snippet zeigt, wie Shear Bottom angepasst wird:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithCylinder-CustomizedShearBottomCylinder-1.py" >}}

! [Todo: image_alt_text](working-with-cylinder_2.png)

Der linke Zylinder hat `shear_bottom` bis (0, 0.83), während der rechte ein Ordnungszylinder ist.
#  **Lüfter zylinder erstellen**
Aspose.3D for Python via .NET ermöglicht die Erstellung eines Lüfter zylinders. Um diese Funktional ität nutzen zu können, können Sie die Eigenschaft `generate_fan_cylinder` der Klasse `Cylinder` auf `True` festlegen. Das folgende Code-Snippet zeigt, wie diese Funktional ität verwendet wird:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithCylinder-CustomizedShearBottomCylinder-1.py" >}}

! [Todo: image_alt_text](working-with-cylinder_3.png)

Der linke Zylinder hat `generate_fan_cylinder = False` und der rechte hat `generate_fan_cylinder = True`.
