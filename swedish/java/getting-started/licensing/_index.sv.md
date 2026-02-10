---
title: Licensing
type: docs
weight: 60
url: /sv/java/licensing/
description: Du kan enkelt ladda ner/installera Aspose.3D for Java från Aspose arkiv för utvärdering. Nedladdningen av utvärderingen är samma som den köpta nedladdningen. Utvärderingsversionen blir helt enkelt licensierad när du lägger till några rader av kod för att tillämpa licensen.
---
##  **Utvärdera Aspose.3D**
Du kan enkelt ladda ner/installera Aspose.3D for Java från [Aspose Arkiv](https://releases.aspose.com/java/repo/com/aspose/aspose-3d/) för utvärdering. Nedladdningen av utvärderingen är samma som den köpta nedladdningen. Utvärderingsversionen blir helt enkelt licensierad när du lägger till några rader av kod för att tillämpa licensen.

Utvärderingsversionen innehåller alla funktioner utom följande:

- Användare kan bara öppna eller importera max 50 3D dokument till en scen.
- Användare kan endast spara högst 50 3D dokument till en scen.
- Användarna kommer också att se en utvärdering vattenstämpel i de återgivna bilderna och alla andra utdatafiler.
- Varje nod får inte ha mer än 5 barnnoder.
- Varje nod kan inte ha mer än 2 bifogade enheter.
- Varje geometri kan inte ha mer än 2 bifogade vertex element.
- Varje nod får inte ha mer än 1 material.

{{% alert color="primary" %}} 

Om du använder Aspose.3D utan en riktig licens, kan det utlösa**com.aspose.threed.TrialException**När användningen nådde de icke-licenserade begränsningarna kan du stänga av undantaget genom att:

* [Köp en fullständig licens](https://purchase.aspose.com/buy).
* Begär en 30 dagars temporär licens, se [Hur får man en tillfällig licens?](https://purchase.aspose.com/temporary-license) För mer information.
.
* Ring `com.aspose.threed.TrialException.setSuppressTrialException(true)` innan dina `open`/`save`-metoder, `TrialException` kommer inte att höjas under `open`/`save` samtalet på Scene, men ovanstående begränsningar kommer inte att upphävas.
* Använd ett block `try/catch` manuellt på `Scene.open/save`, det här undantaget är bara en meddelande, ignorera det kommer inte att påverka scenen ladda/spara.

{{% /alert %}} 
##  **Använda licens**
Licensen är en enkel text XML-fil som innehåller detaljer såsom produktnamnet, antal utvecklare den är licensierad till, prenumerationsdatum och så vidare. Filen är digitalt signerad, så ändra inte filen. även oavsiktligt tillägg av en extra radbrytning i filen kommer att ogiltigförklara den. Du måste ställa in en licens innan du utför någon operation med dokument. Se till att du gör detta innan du skapar ett Scene-objekt.

Licenser kan tillämpas från olika platser:

- Explicit sökvägName
- Korgen som innehåller Aspose.3D s JAR-fil.
- En inbäddad resurs i JAR som kallade Aspose.3D JAR.

Använd `License.setLicense`-metoden för att licensiera API:erna. Det enklaste sättet att ställa in en licens är ofta att placera licensfilen i samma mapp som Aspose. 3D är JAR och ange bara filnamnet utan sökväg.
###  **Använd licens med fil eller strömobjekt**
In this example Aspose.3D will attempt to find the license file in the folder that contain the JARs of your application.

{{< highlight "java" >}}
License license = new License();
license.setLicense("Aspose._3D.lic");
{{< /highlight >}}

Initierar en licens från en ström.

{{< highlight "java" >}}
License license = new License();
try(FileInputStream myStream = new FileInputStream("Aspose._3D.lic")) {
    license.setLicense(myStream);
}
{{< /highlight >}}
###  **Inklusive licensfilen som en inbäddad resurs.**
Du kan helt enkelt kopiera LIC-filen i katalogen `resources` i ditt projekt. Att återuppbygga projektet bör inbädda . Lic-fil till applikations . Burkfil. Därefter kan du ansöka om licens genom att använda koden som nedan:

{{< highlight "java" >}}
License lic = new License();
lic.setLicense(Program.class.getResourceAsStream("Aspose.3D.Java.lic"));
{{< /highlight >}}
###  **Validera licensen**
Det är möjligt att validera om licensen har satts ordentligt eller inte. Licensklassen har isLicensed-fältet som kommer att returnera true om licensen har satts ordentligt.

{{< highlight "java" >}}
License license = new License();
license.setLicense("Aspose.3D.Java.lic");
    	  
if (License.isLicenseSet()) {
    System.out.println("License is Set!");
}
{{< /highlight >}}
##  **Använd mätt licens**
Aspose.3D tillåter utvecklare att använda uppmätta nyckel. Det är en ny licensmekanism. Den nya tillståndsmekanismen kommer att användas tillsammans med befintlig tillståndsmetod. De kunder som vill faktureras baserat på användningen av API-funktionerna kan använda den mättade licensieringen. För mer information, se [Uppmätt Licensing FAQ](https://purchase.aspose.com/faqs/licensing/metered) avsnittet.

En ny klass `Metered` har introducerats för att tillämpa mättad nyckel. Följande är urvalskoden som visar hur man ställer in öppen och privat nyckel.

{{< highlight "java" >}}
// Initialize a Metered license class object
Metered metered = new Metered();
// Set public and private keys
metered.setMeteredKey("your-public-key", "your-private-key");
{{< /highlight >}}
##  **När du ska använda licens**
Följ dessa enkla regler:

- Licensen behöver bara ställas in en gång per ansökningsdomän.
- Du måste ställa in licensen innan du använder några andra Aspose.3D klasser.
- Ring licens.SetLicense flera gånger är inte skadligt, men helt enkelt slösar processortid.

Om du utvecklar ett klassbibliotek kan du ringa Licens. Ange licens från en statisk konstruktör i klassen som använder Aspose. 3D. Den statiska konstruktorn körs innan en instans i klassen skapas för att se till att Aspose.3D licens är riktigt inställd.
##  **Du kan ändra licensfilnamn**
Namnet på licensfilen behöver inte vara 'Aspose.3D.LIC'. Du kan byta namn till vad du vill och använda det namnet när du ringer licens.SetLicense.
##  **Undantag kan inte hitta licensfilnamn**
När du köper och laddar ner en licens, Aspose namngiver licensfilen `Aspose.3D.LIC`. Du laddar ner licensfilen med din webbläsare. Vissa webbläsare känner igen licensfilen som XML och lägg till en . Xml tillägg till det så att det fullständiga namnet på filen på datorn blir `Aspose.3D.lic.XML`.

När Microsoft Windows, till exempel, är konfigurerad för att dölja filändelser av kända filtyper (det är tyvärr standard i de flesta Windows installationer), licensfilen kommer att användas för dig som `Aspose.3D.LIC` i Windows Explorer. Du tror sannolikt att detta är det riktiga filnamnet och samtal licens. SetLicense skickar det `Aspose.3D.LIC`, men det finns ingen sådan fil, därav undantaget.

För att lösa problemet, byta namn på filen för att ta bort den osynliga . Xml- utökning. Vi rekommenderar också att du inaktiverar alternativet " dole tillägg" i Microsoft Windows.

##  **Använder flera API från Aspose.**
Om du använder flera Aspose API i programmet, till exempel Aspose. 3D och Aspose. Cells, här är några användbara tips.

- Ange licensen för varje Aspose API separat. Även om du har en enda licensfil för alla API, till exempel `Aspose.Total.lic`, du behöver fortfarande ringa `License.setLicense` separat för varje Aspose API du använder i ditt program.
- Använd fullt kvalificerad licensklass namn. Varje Aspose API har en licensklass i sin namnrymd. Till exempel har Aspose.3D `com.aspose.3d.License` och Aspose.Cells har klass `com.aspose.cells.License`. Genom att använda det fullt kvalificerade klassnamnet kan du undvika all förvirring om vilken licens som tillämpas på vilken produkt.
