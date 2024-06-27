---
title: Licensing
type: docs
weight: 60
url: /sv/net/licensing/
description: Översikt av Licensing Krav och utvärderingsversionsbegränsningar för behandling av 3D filformat i C#.
---
Översikt av Licensing Krav och utvärderingsversionsbegränsningar för behandling av 3D filformat i C#.

##  **Utvärderingsversionsbegränsningar**
En kostnadsfri utvärderingsversion av Aspose. 3D for .NET kan laddas ner från nedladdningsavsnittet på Asposes webbplats på: [Ladda ner Aspose.3D API](https://www.nuget.org/packages/Aspose.3D).
###  **Begränsning**
Utvärderingsversionen innehåller alla funktioner utom följande:

- Användare kan bara öppna/importera högst 50 3D dokument till en scen.
- Varje nod får inte ha mer än 5 barnnoder.
- Varje nod kan inte ha mer än 2 bifogade enheter.
- Varje geometri kan inte ha mer än 2 bifogade vertex element.
- Varje nod får inte ha mer än 1 material.
- Användare kan bara spara högst 50 3D dokument till en scen.
- Användarna kommer också att se en utvärdering vattenstämpel i de återgivna bilderna och alla andra utdatafiler.

{{% alert color="primary" %}} 
Om du använder Aspose. 3D utan en riktig licens kan det utlösa en `Aspose.ThreeD.TrialException` när användningen nådde de icke-licenserade begränsningarna, du kan stänga av undantaget genom att:

* [Köp en fullständig licens](https://purchase.aspose.com/buy).
* Begär en 30 dagars temporär licens, se [Hur får man en tillfällig licens?](https://purchase.aspose.com/temporary-license) För mer information.
.
* Ställ in `Aspose.ThreeD.TrialException.SuppressTrialException` till `true`. `TrialException` kommer inte att höjas under `Open/Save` samtalen i scenen, men ovanstående begränsningar kommer inte att upphävas.
* Använd ett block `try/catch` manuellt på `Scene.Open/Save`, det här undantaget är bara en meddelande, ignorera det kommer inte att påverka scenen ladda/spara.

{{% /alert %}} 

##  **Använd licens med fil eller strömobjekt**
Licensen kan laddas från en [Fil](https://docs.aspose.com/3d/net/licensing/#Licensing-LoadingaLicensefromFile) eller [Strömobjekt](https://docs.aspose.com/3d/net/licensing/#Licensing-LoadingaLicensefromaStreamObject). Aspose.3D for .NET kommer att försöka hitta licensen på följande platser:

1. Explicit väg.
1. Korgen som innehåller Aspose.3D.dll.
1. Korgen som innehåller monteringen som kallade Aspose.3D.dll.
1. Korgen som innehåller inmatningssammansättningen (din . Exe.
1. En inbäddad resurs i monteringen som kallade Aspose.3D.dll.

Det enklaste sättet att ställa in en licens är att placera licensfilen i samma mapp som Aspose. 3D. dll filen och ange filnamnet, utan sökväg, som visas i exemplet nedan.

{{% alert color="primary" %}} 

Om du använder någon annan Aspose for .NET API tillsammans med Aspose. 3D for .NET, ange namnrymden för licensen som `Aspose.ThreeD.License`.

{{% /alert %}} 
###  **Laddar en licens från fil**
Det enklaste sättet att tillämpa en licens är att placera licensfilen i samma mapp som Aspose. 3D. dll filen och ange bara filnamnet utan sökväg.

{{% alert color="primary" %}} 

När du ringer `SetLicense`-metoden, ska licensnamnet som du skickar över vara det i licensfilen. Om du till exempel ändrar namnet på licensfilen till "Aspose.3D.lic.xml" skickar filnamnet till `threeD.SetLicense(…)`-metoden.

{{% /alert %}} 

**Exempel:**

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-License-ApplyLicense-ApplyLicenseUsingFile.cs" >}}
###  ` `**Ladda en licens från ett strömobjekt**
Följande exempel visar hur man laddar en licens från en ström.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-License-ApplyLicense-ApplyLicenseUsingStreamObject.cs" >}}
##  **Använd licens med inbäddad resurs.**
Ett sätt att tillämpa en licens är att ställa in den [Använder ett fil eller ett strömobjekt](). Ett annat snyggt sätt att förpacka licensen med din ansökan och se till att det inte kommer att förloras är att inkludera den som en inbäddad resurs. in i en av de sammansättningar som kallar komponentens DLL (inklusive i Aspose. 3D)

För att inkludera licensfilen som en inbäddad resurs:

1. I Visual Studio .NET, inkludera licensfilen (.lic) i projektet genom att välja.**Arkiv**, Sedan**Lägg till befintlig objekt**Och slutligen.**Lägg till**.
1. Välj filen i Lösningsutforskaren.
1. Ange**Bygg åtgärd**Till följd**Inbäddad resursName**I fönstret Egenskaper.
1. För att komma åt licensen inbäddad i monteringen (som en inbäddad resurs), lägg bara till licensfilen som en inbäddad resurs till projektet och skicka namnet på licensfilen till SetLicense-metoden. Licensklassen hittar automatiskt licensfilen i de inbäddade resurserna. Det finns ingen anledning att kalla GetExecutingAmonty och GetManifestResourceStream metoder för systemet. Reflektion. Monteringsklass i Microsoft .NET ramverket.

Följande kod snippet används för att ställa in licensen.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-License-ApplyLicense-ApplyLicenseUsingEmbeddedResource.cs" >}}
##  **Använd mätt licens**
Aspose.3D for .NET API tillåter utvecklare att applicera uppmätta licens. Det är en ny licensmekanism. Den nya tillståndsmekanismen kommer att användas tillsammans med befintlig tillståndsmetod. De kunder som vill faktureras baserat på användningen av API-funktionerna kan använda den mättade licensieringen. För mer information, se [Uppmätt Licensing FAQ](https://purchase.aspose.com/faqs/licensing/metered) avsnittet.

En ny klass [`Metered`](https://reference.aspose.com/3d/net/aspose.threed/metered) har lagts till för att applicera uppmätta nyckel. Detta kodexempel visar hur man anger offentliga och privata nycklar:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-License-ApplyLicense-PublicAndPrivateKeys.cs" >}}
