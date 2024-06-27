---
title: Arbeta med cylinder
type: docs
weight: 130
url: /sv/net/working-with-cylinder/
description: Aspose.3D for .NET tillåter anpassning av offset Topp i en cylinder. För att använda denna funktionalitet kan du använda Offset egenskap av Cylinderklass.
---
#  **Anpassa offset övrev**
Aspose.3D for .NET tillåter anpassning av offset Topp i en cylinder. För att kunna använda denna funktionalitet, kan du använda `Offset` egenskapen i `Cylinder` klassen. Följande kod snutt visar hur man anpassar Offset Top:



{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-WorkingWithCylinder-CustomizedOffsetTopCylinder-1.cs" >}}

![todo:image_alt_text](working-with-cylinder_1.png)

Den vänstra har OffsetTop satt till (5, 3, 0), Det är lätt att se att topplocket har flyttat och hela bålet påverkas också.
#  **Anpassa shearBottom**
Aspose.3D for .NET tillåter anpassning av skjuvningsbotten på en cylinder. För att kunna använda denna funktionalitet, kan du använda `ShearBottom` egenskapen i `Cylinder` klassen. Följande kodutdrag visar hur man anpassar skjuv nedre:



{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-WorkingWithCylinder-CustomizedShearBottomCylinder-1.cs" >}}

![todo:image_alt_text](working-with-cylinder_2.png)

Den vänstra cylindern har `ShearBottom` till (0, 0.83) medan den högra är en ordinarie cylinder.
#  **Skapa fläkt- cylinder**
Aspose.3D for .NET tillåter skapandet av en fläktcylinder. För att kunna använda denna funktionalitet, kan du ställa in `GenerateFanCylinder` egenskap av `Cylinder` klass till `true`. Följande kodsnutt visar hur denna funktionalitet ska användas:



{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-WorkingWithCylinder-CustomizedShearBottomCylinder-1.cs" >}}

![todo:image_alt_text](working-with-cylinder_3.png)

Den vänstra cylindern har `GenerateFanCylinder = false` och den högra har `GenerateFanCylinder = true`.
