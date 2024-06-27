---
title: Ditt första Aspose.3D-program
type: docs
weight: 30
url: /sv/java/your-first-aspose-3d-application/
description: Skapa, redigera och spara din första 3d-fil i vilka format som stöds med hjälp av Aspose. 3D for Java för att uppleva dess enkelhet och kraft i Java.
keywords: Java , Aspose.3D for Java , The first application using Aspose.3D for Java, The first program via Aspose.3D for Java.
---
{{% alert color="primary" %}}

Den här handledningen förklarar hur ditt första program skapas med Aspose.3Ds enkla API. Detta enkla program skapar en 3D-fil i en angiven 3D-scen.

{{% /alert %}}

##  **Hur man skapar programmet**

Stegen nedan skapar programmet med Aspose.3D API:

1. Skapa en instans av [Scene](https://reference.aspose.com/3d/java/com.aspose.threed/scene/)-klassen.
1. Om du har en licens, då [Tillämpa den](/3d/sv/java/licensing/).
Om du använder utvärderingsversionen, hoppa över licensrelaterade kodlinjer.
1. Skapa en ny 3D-fil, eller öppna en befintlig 3D-fil.
1. Åtkomst till innehållet i filen 3D.
1. Skapa den ändrade 3D-filen.

Genomförandet av ovanstående steg visas i exemplen nedan.

###  **Hur man skapar ett nytt scendokument**

Följande exempel skapar en ny 3D scenefil från början. Skapa först en 3D-scen och sedan spara filen i FBX-format.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-CreateEmpty3DDocument.java" >}}

###  **Hur man öppnar en befintlig fil**

The following example opens an existing 3D template file named "document.fbx" and then saves the 3D scene or document to a stream in various supported 3D formats.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-Save3DScene.java" >}}
