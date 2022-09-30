---
title: Arbeiten mit Zylinder
type: docs
weight: 100
url: /de/java/working-with-cylinder/
description: Aspose.3D for Java ermöglicht das Anpassen der Offset-Oberseite eines Zylinders. Um diese Funktional ität zu nutzen, können Sie die setOffsetTop()-Methode der Cylinder-Klasse verwenden.
---
# **Offset-Top anpassen**
Aspose.3D for Java ermöglicht das Anpassen der Offset-Oberseite eines Zylinders. Um diese Funktional ität zu nutzen, können Sie die Methode `setOffsetTop()` der Klasse `Cylinder` verwenden. Das folgende Code-Snippet zeigt, wie Offset Top angepasst wird:



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "CustomizedOffsetTopCylinder.java" >}}

![Todo: bild_Alt_Text](working-with-cylinder_1.png)

Im linken ist OffsetTop auf (5, 3, 0) eingestellt. Es ist leicht zu erkennen, dass sich die obere Kappe bewegt hat und auch der gesamte Torso betroffen ist.
# **Shear Bottom anpassen**
Aspose.3D for Java ermöglicht die Anpassung des Scher bodens eines Zylinders. Um diese Funktional ität zu nutzen, können Sie die Eigenschaft `setShearBottom()` der Klasse `Cylinder` verwenden. Das folgende Code-Snippet zeigt, wie Shear Bottom angepasst wird:



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "CustomizedShearBottomCylinder.java" >}}

![Todo: bild_Alt_Text](working-with-cylinder_2.png)

Der linke Zylinder hat Shear Bottom bis (0, 0,83), während der rechte ein Ordnungszylinder ist.
# **Lüfter zylinder erstellen**
Aspose.3D for Java ermöglicht die Schaffung eines Lüfter zylinders. Um diese Funktional ität zu nutzen, können Sie `setGenerateFanCylinder()` Eigenschaft der `Cylinder` Klasse bis `true`. Das folgende Code-Snippet zeigt, wie diese Funktional ität verwendet wird:



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "CreateFanCylinder.java" >}}

![Todo: bild_Alt_Text](working-with-cylinder_3.png)

Der linke Zylinder hat Generate Fan Cylinder = falsch und der rechte hat Generate Fan Cylinder = wahr.
