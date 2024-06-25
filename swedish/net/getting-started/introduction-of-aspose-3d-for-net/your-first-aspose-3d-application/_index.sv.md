---
title: Ditt första Aspose.3D-program
type: docs
weight: 30
url: /sv/net/your-first-aspose-3d-application/
description: Skapa, redigera och spara din första 3d-fil i vilka format som stöds med hjälp av Aspose. 3D for .NET för att uppleva dess enkelhet och kraft i C#.
keywords: C# , Aspose.3D for .NET , The first application using Aspose.3D for .NET, The first program via Aspose.3D for .NET.
---
{{% alert color="primary" %}}

Den här handledningen förklarar hur ditt första program skapas med Aspose.3Ds enkla API. Detta enkla program skapar en 3D-fil i en angiven 3D-scen.

{{% /alert %}}

##  **Hur man skapar programmet**

Stegen nedan skapar programmet med Aspose.3D API:

1. Skapa en instans av [Scene](https://reference.aspose.com/3d/net/aspose.threed/scene/)-klassen.
1. Om du har en licens, då [Tillämpa den](/3d/sv/net/licensing/).
Om du använder utvärderingsversionen, hoppa över licensrelaterade kodlinjer.
1. Skapa en ny 3D-fil, eller öppna en befintlig 3D-fil.
1. Åtkomst till innehållet i filen 3D.
1. Skapa den ändrade 3D-filen.

Genomförandet av ovanstående steg visas i exemplen nedan.

###  **Hur man skapar ett nytt scendokument**

Följande exempel skapar en ny 3D scenefil från början. Skapa först en 3D-scen och sedan spara filen i FBX-format.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-CreateEmpty3DDocument-CreateEmpty3DDocument.cs" >}}

###  **Hur man öppnar en befintlig fil**

The following example opens an existing 3D template file named "document.fbx" and then saves the 3D scene or document to a stream in various supported 3D formats.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-Save3DScene-Save3DScene.cs" >}}
