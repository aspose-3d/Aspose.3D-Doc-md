---
title: Licensiering
type: docs
weight: 60
url: /sv/net/licensing/
description: Översikt över licenskrav och utvärderingsversion Begränsningar för behandling 3D filformat i C#.
---
Översikt över licenskrav och utvärderingsversion Begränsningar för behandling 3D filformat i C#.

## **Utvärderingsversionsbegränsningar**
En kostnadsfri utvärderingsversion av Aspose.3D for .NET kan laddas ner från nedladdningar av Aspose webbplats på:[Ladda ner Aspose.3D API](https://www.nuget.org/packages/Aspose.3D).
### **Begränsning**
Utvärderingsversionen innehåller alla funktioner utom följande:

- Användare kan endast öppna/importera högst 50 3D dokument till en Scene.
- Varje nod får inte ha mer än 5 barnnoder.
- Varje nod kan inte ha mer än 2 bifogade enheter.
- Varje geometri kan inte ha mer än 2 bifogade vertex element.
- Varje nod får inte ha mer än 1 material.
- Användare kan endast spara högst 50 3D dokument till en Scene.
- Användarna kommer också att se en utvärdering vattenstämpel i de återgivna bilderna och alla andra utdatafiler.

{{% alert color="primary" %}} 
Om du använder Aspose.3D utan rätt körkort, det skulle kunna utlösa en `Aspose.ThreeD.TrialException` när användningen nådde de olicensierade begränsningarna, kan du stänga av undantaget genom:

* [Köp en fullständig licens](https://purpose.aspose.com/buy).
* Begär en 30 dagars tillfällig licens, se [Hur får man en tillfällig licens?] (https://köp. Förmodligen. För mer information.
.
* Set 'Aspose.ThreeD. Testavvikelse. "Suppress TrialException" till "true", "TrialException" kommer inte att höjas under utlysningen "Open/Save" på Scene, men ovanstående begränsningar kommer inte att upphävas.
* Använd manuellt ett "försök/catch"-block på "Scene. Öppna/Save', detta undantag är bara en anmälan, ignorera det kommer inte att påverka scenen ladda / spara.

{{% /alert %}} 

## **Använd licens med fil eller strömobjekt**
Licensen kan laddas från en[Fil](https://docs.aspose.com/3d/net/licensing/#Licensing-LoadingaLicensefromFile)Eller[Strömobjekt](https://docs.aspose.com/3d/net/licensing/#Licensing-LoadingaLicensefromaStreamObject). Aspose.3D for .NET kommer att försöka hitta licensen på följande platser:

1. Explicit väg.
1. Katalogen som innehåller Aspose.3D.dll.
1. Mappen som innehåller monteringen som heter Aspose.3D.dll.
1. Korgen som innehåller inmatningssammansättningen (din . Exe.
1. En inbäddad resurs i monteringen som kallades Aspose.3D.dll.

Det enklaste sättet att ställa in en licens är att placera licensfilen i samma mapp som Aspose.3D. dll filen och ange filnamnet, utan sökväg, som visas i exemplet nedan.

{{% alert color="primary" %}} 

Om du använder någon annan Aspose for .NET API tillsammans med Aspose.3D 076143488 1, ange namnrymden för licensen som `Aspose.ThreeD.License`.

{{% /alert %}} 
### **Laddar en licens från fil**
Det enklaste sättet att tillämpa en licens är att placera licensfilen i samma mapp som Aspose.3D. dll filen och ange bara filnamnet utan sökväg.

{{% alert color="primary" %}} 

När du ringer `SetLicense` metoden, licensnamnet som du skickar ska vara den i licensfilen. Till exempel, om du ändrar licensfilnamnet till "Aspose.3D.lic.xml" skickar filnamnet till `threeD.SetLicense(…)` metod.

{{% /alert %}} 

**Exempel:**

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-License-ApplyLicense-ApplyLicenseUsingFile.cs" >}}
### ` `**Ladda en licens från ett strömobjekt**
Följande exempel visar hur man laddar en licens från en ström.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-License-ApplyLicense-ApplyLicenseUsingStreamObject.cs" >}}
## **Använd licens med inbäddad resurs.**
Ett sätt att tillämpa en licens är att ställa in den[Använder ett fil eller ett strömobjekt](). Ett annat snyggt sätt att förpacka licensen med din ansökan och se till att det inte kommer att förloras är att inkludera den som en inbäddad resurs. i en av de sammansättningar som kallar komponentens DLL (inklusive i Aspose.3D).

För att inkludera licensfilen som en inbäddad resurs:

1. I Visual Studio .NET, inkludera licensfilen (.lic) i projektet genom att välja licensfilen.**Arkiv**, Sedan**Lägg till befintlig objekt**Och slutligen.**Lägg till**.
1. Välj filen i Lösningsutforskaren.
1. Ange**Bygg åtgärd**Till följd**Inbäddad resursName**I fönstret Egenskaper.
1. För att komma åt licensen inbäddad i monteringen (som en inbäddad resurs), lägg bara till licensfilen som en inbäddad resurs till projektet och skicka namnet på licensfilen till SetLicense-metoden. Licensklassen hittar automatiskt licensfilen i de inbäddade resurserna. Det finns ingen anledning att kalla GetExecutingAmonty och GetManifestResourceStream metoder för systemet. Reflektion. Församlingsklass i Microsoft .NET rambestämmelser.

Följande kod snippet används för att ställa in licensen.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-License-ApplyLicense-ApplyLicenseUsingEmbeddedResource.cs" >}}
## **Använd mätt licens**
Aspose.3D for .NET API gör det möjligt för utvecklare att tillämpa uppmätta licens. Det är en ny licensmekanism. Den nya tillståndsmekanismen kommer att användas tillsammans med befintlig tillståndsmetod. De kunder som vill faktureras baserat på användningen av API funktioner kan använda den mättade licensieringen. För ytterligare upplysningar, se på[Uppmätt licensiering](https://purchase.aspose.com/faqs/licensing/metered)Sektion.

En ny klass [`Metered`](https://reference.aspose.com/3d/net/aspose.threed/metered) har lagts till för att applicera mättad nyckel. Detta kodexempel visar hur man anger offentliga och privata nycklar:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-License-ApplyLicense-PublicAndPrivateKeys.cs" >}}
