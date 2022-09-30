---
title: Arbeta med cylinder
type: docs
weight: 130
url: /sv/python-net/working-with-cylinder/
description: Aspose.3D för Python via .NET tillåter anpassning Offset Toppen av en cylinder. För att använda denna funktionalitet kan du använda Offset egenskap av Cylinderklass.
---
# **Anpassa offset övrev**
Aspose.3D för Python via .NET tillåter anpassning Offset Toppen av en cylinder. För att använda denna funktionalitet, kan du använda `offset` fastighet av `Cylinder` klass. Följande kod snutt visar hur man anpassar Offset Top:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithCylinder-CustomizedOffsetTopCylinder-1.py" >}}

![TOD:imageName_Av_Text:](working-with-cylinder_1.png)

Den vänstra har `offset_top` inställd på (5, 3, 0), Det är lätt att se att topplocket har flyttat och hela bålet påverkas också.
# **Anpassa shearBottom**
Aspose.3D för Python via .NET gör det möjligt att anpassa skjuv botten på en cylinder. För att använda denna funktionalitet, kan du använda `shear_bottom` fastighet av `Cylinder` klass. Följande kodutdrag visar hur man anpassar skjuv nedre:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithCylinder-CustomizedShearBottomCylinder-1.py" >}}

![TOD:imageName_Av_Text:](working-with-cylinder_2.png)

Den vänstra cylindern har `shear_bottom` till (0, 0,83) medan den högra är en vanlig cylinder.
# **Skapa fläkt- cylinder**
Aspose.3D för Python via .NET gör det möjligt att skapa en fläktcylinder. För att använda denna funktionalitet, kan du ställa in `generate_fan_cylinder` objekt av `Cylinder` klass till `True`. Följande kodsnutt visar hur denna funktionalitet ska användas:



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "WorkingWithCylinder-CustomizedShearBottomCylinder-1.py" >}}

![TOD:imageName_Av_Text:](working-with-cylinder_3.png)

Den vänstra cylindern har `generate_fan_cylinder = False` och den högra har `generate_fan_cylinder = True`.
