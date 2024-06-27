---
title: Arbeta med cylinder
type: docs
weight: 100
url: /sv/java/working-with-cylinder/
description: Aspose.3D for Java tillåter anpassning av offset Topp i en cylinder. För att använda denna funktionalitet, kan du använda setOffsetTop () metod för cylinderklass.
---
#  **Anpassa offset övrev**
Aspose.3D for Java tillåter anpassning av offset Topp i en cylinder. För att kunna använda denna funktionalitet kan du använda `setOffsetTop()`-metoden för klassen `Cylinder`. Följande kod snutt visar hur man anpassar Offset Top:



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "CustomizedOffsetTopCylinder.java" >}}

![todo:image_alt_text](working-with-cylinder_1.png)

Den vänstra har OffsetTop satt till (5, 3, 0), Det är lätt att se att topplocket har flyttat och hela bålet påverkas också.
#  **Anpassa shearBottom**
Aspose.3D for Java tillåter anpassning av skjuvningsbotten på en cylinder. För att kunna använda denna funktionalitet, kan du använda `setShearBottom()` egenskapen i `Cylinder` klassen. Följande kodutdrag visar hur man anpassar skjuv nedre:



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "CustomizedShearBottomCylinder.java" >}}

![todo:image_alt_text](working-with-cylinder_2.png)

Den vänstra cylindern har ShearBottom till (0, 0.83) medan den högra är en vanlig cylinder.
#  **Skapa fläkt- cylinder**
Aspose.3D for Java tillåter skapandet av en fläktcylinder. För att använda denna funktionalitet kan du `setGenerateFanCylinder()` egenskap av `Cylinder` klass till `true`. Följande kodsnutt visar hur denna funktionalitet ska användas:



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "CreateFanCylinder.java" >}}

![todo:image_alt_text](working-with-cylinder_3.png)

Den vänstra cylindern har GenerateFanCylinder = false och den högra har GenerateFanCylinder = true.
