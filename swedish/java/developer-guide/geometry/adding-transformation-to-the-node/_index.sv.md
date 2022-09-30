---
title: Lägga till omvandling i noden
type: docs
weight: 10
url: /sv/java/adding-transformation-to-the-node/
description: Aspose.3D for Java API har stöd för att rotera objekt i 3D utrymme. Det finns tre sätt att definiera objekts rotation i 3D utrymme, Euler vinklar, Quaternion och Custom Matrix, Alla stöds av Transform-klassen.
---
{{% alert color="primary" %}} 

Aspose.3D for Java API har stöd för att rotera objekt i 3D utrymme. Det finns tre sätt att definiera objekts rotation i 3D utrymme, Euler vinklar, Quaternion och Custom Matrix, Alla stöds av klassen `Transform`.

{{% /alert %}} 

TSR (översättning/Scaling/Rotation) används oftast i 3D scenario, vi tillhandahöll en klass `Transform` för att komma åt dessa i Aspose.3D Affina omvandlingar inkluderar:

- Översättning
- Skalning
- Rotationer
- Skjut avbildning
- Tryck på kartläggning

{{% alert color="primary" %}} 

Klassobjektet `Mesh` används i koden. Vi kan det.[Skapa ett Mesh-klassobjekt som berättat där.](https://docs.dynabic.com/display/3djava/Create+3D+Mesh+and+Scene).

{{% /alert %}} 
## **Rotera med kvittering**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-AddTransformationToNodeByQuaternion.java" >}}
## **Rotera med Euler vinklar**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-AddTransformationToNodeByEulerAngles.java" >}}
## **Egen omvandlingsmatris**
Vi kan också använda Matrix direkt:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-AddTransformationToNodeByTransformationMatrix.java" >}}
