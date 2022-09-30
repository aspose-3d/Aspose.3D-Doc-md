---
title: Arbeta med cylinder
type: docs
weight: 100
url: /sv/java/working-with-cylinder/
description: Aspose.3D for Java tillåter anpassning Offset Toppen av en cylinder. För att använda denna funktionalitet, kan du använda setOffsetTop () metod för cylinderklass.
---
# **Anpassa offset övrev**
Aspose.3D for Java tillåter anpassning Offset Toppen av en cylinder. För att använda denna funktionalitet, kan du använda `setOffsetTop()` metod av `Cylinder` klass. Följande kod snutt visar hur man anpassar Offset Top:



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "CustomizedOffsetTopCylinder.java" >}}

![TOD:imageName_Av_Text:](working-with-cylinder_1.png)

Den vänstra har OffsetTop satt till (5, 3, 0), Det är lätt att se att topplocket har flyttat och hela bålet påverkas också.
# **Anpassa shearBottom**
Aspose.3D for Java gör det möjligt att anpassa skjuv botten på en cylinder. För att använda denna funktionalitet, kan du använda `setShearBottom()` fastighet av `Cylinder` klass. Följande kodutdrag visar hur man anpassar skjuv nedre:



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "CustomizedShearBottomCylinder.java" >}}

![TOD:imageName_Av_Text:](working-with-cylinder_2.png)

Den vänstra cylindern har ShearBottom till (0, 0.83) medan den högra är en vanlig cylinder.
# **Skapa fläkt- cylinder**
Aspose.3D for Java gör det möjligt att skapa en fläktcylinder. För att använda denna funktionalitet, kan du `setGenerateFanCylinder()` fastighet av `Cylinder` klass till `true`. Följande kodsnutt visar hur denna funktionalitet ska användas:



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "CreateFanCylinder.java" >}}

![TOD:imageName_Av_Text:](working-with-cylinder_3.png)

Den vänstra cylindern har GenerateFanCylinder = false och den högra har GenerateFanCylinder = true.
