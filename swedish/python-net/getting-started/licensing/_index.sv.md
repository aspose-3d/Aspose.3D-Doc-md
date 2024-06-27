---
title: Licensing
description: Aspose.3D for Python via .NET tillhandahåller olika planer för köp eller erbjuder en gratis rättegång och en 30-dagars temporär licens för utvärdering med Licensing och abonnemangspolicy
type: docs
weight: 80
url: /sv/python-net/licensing/
---
Ibland, för att studera systemet bättre, du vill dyka in i koden så snabbt som möjligt. För att underlätta detta, Aspose. 3D tillhandahåller olika planer för köp eller erbjuder en gratis rättegång och en 30-dagars temporär licens för utvärdering.

{{% alert color="primary" %}}

Observera att det finns ett antal allmänna policyer och praxis som vägleder dig om hur du utvärderar, licensierar och köper våra produkter. Du hittar dem i avsnittet ["Inköpspolicyer och FAQ"](https://purchase.aspose.com/policies).

{{% /alert %}}

##  **Utvärdera Aspose.3D**
Du kan enkelt ladda ner Aspose.3D för utvärdering. Utvärderingspaketet är detsamma som det köpta paketet. Utvärderingsversionen blir helt enkelt licensierad när du lägger till några rader av kod för att tillämpa licensen.

##  **Utvärderingsversionsbegränsning**
Utvärderingsversionen innehåller alla funktioner utom följande:

- Användare kan bara öppna/importera högst 50 3D dokument till en scen.
- Varje nod får inte ha mer än 5 barnnoder.
- Varje nod kan inte ha mer än 2 bifogade enheter.
- Varje geometri kan inte ha mer än 2 bifogade vertex element.
- Varje nod får inte ha mer än 1 material.
- Användare kan bara spara högst 50 3D dokument till en scen.
- Användarna kommer också att se en utvärdering vattenstämpel i de återgivna bilderna och alla andra utdatafiler.

{{% alert color="primary" %}} 
Om du använder Aspose. 3D utan en riktig licens kan det utlösa en `aspose.threed.TrialException` när användningen nådde de icke-licenserade begränsningarna, du kan stänga av undantaget genom att:

* [Köp en fullständig licens](https://purchase.aspose.com/buy).
* Begär en 30 dagars temporär licens, se [Hur får man en tillfällig licens?](https://purchase.aspose.com/temporary-license) För mer information.
* Använd ett block `try/except` manuellt på `Scene.open/save`, det här undantaget är bara en meddelande, ignorera det kommer inte att påverka scenen ladda/spara.

{{% /alert %}} 


##  **Om licensen**
Du kan enkelt ladda ner en utvärderingsversion av Aspose.3D for Python via .NET från dess [Ladda ner sidan](https://pypi.org/project/aspose.3d/). Utvärderingsversionen ger absoluta**Samma förmågar**Som den licensierade versionen av Aspose.3D. Dessutom: utvärderingsversionen blir helt enkelt licensierad efter att du köper en licens och lägga till ett par rader av kod för att tillämpa licensen ..

Licensen är enkel text XML-fil som innehåller detaljer såsom produktnamnet, antal utvecklare den är licensierad till, prenumerationsdatum, och så vidare. Filen är digitalt signerad, så ändra inte filen. Även ett oavsiktligt tillägg av en extra radbrytning till innehållet i filen kommer att ogiltigförklara den.

För att undvika begränsningarna i samband med utvärderingsversionen måste du ställa in en licens innan du används**Aspose.3D**. Du behöver bara ställa in en licens en gång per ansökan eller process.

## Köpt licens

Efter köpet måste du tillämpa licensfilen eller strömmen. I detta avsnitt beskrivs alternativ för hur detta kan göras, och även kommentarer till vissa vanliga frågor.

{{% alert color="primary" %}}

Du måste ställa in licensen:
* Endast en gång per programdomänen
* Innan någon annan Aspose.3D klasser

{{% /alert %}}

{{% alert color="primary" %}}

Du hittar prisuppgifter på sidan [’Prisuppgifter’](https://purchase.aspose.com/pricing/3d/family).

{{% /alert %}}

###  **Ställer in en licens i Aspose.3D for Python via .NET?**

Licenser kan tillämpas från olika platser:

* Explicit sökvägName
* Korgen som innehåller python- skriptet som ringer Aspose.3D for Python via .NET.
* Ström
* Som en meterad licens - en ny licensmekanism för licens

{{% alert color="primary" %}}

Använd `set_license`-metoden för att licensiera en komponent.

Att ringa `set_license` flera gånger är inte skadligt, det slösar bara processortid.

{{% /alert %}}

I avsnitten nedan beskriver vi de två gemensamma metoderna för att ställa in licensen.

####  **Tillämpa en licens med hjälp av en fil**
Den enklaste metoden för att ställa in en licens kräver att du placerar licensfilen i samma korg som innehåller python-skriptet som ringer Aspose. .. 3D för Python och ange bara filnamnet utan sökväg.

Denna kodsnutt används för att ange en licensfil:

**Python**

```py
import aspose.threed as a3d

# Instantiate an instance of license and set the license file through its path
license = a3d.License()
license.set_license("Aspose.3D.lic")
```

När du ringer `set_license`-metoden ska licensnamnet vara samma som i din licensfil. Du kan till exempel ändra licensfilnamnet till "Aspose.3D.lic.xml". Sedan, i koden, måste du skicka det nya licensnamnet (Aspose. 3D. - Lik. xml) till SetLicense-metoden.

####  **Tillämpa en licens från en ströma**
Du kan ladda licens från en ström.

Denna kodsnutt används för att tillämpa en licens från en ström:

**Python**

```py
import aspose.threed as a3d

# Instantiate an instance of license and set the license file through its path
license = a3d.License()
license.set_license(stream)
```

#### Använd mätt licens

Aspose.3D tillåter utvecklare att använda en uppmätta nyckel. Detta är en ny licensmekanism.

Den nya tillståndsmekanismen kommer att användas tillsammans med den befintliga tillståndsmetoden. De kunder som vill faktureras baserat på användningen av API-funktioner kan använda uppmätta Licensing.

Efter att ha slutfört alla nödvändiga steg för att få denna typ av licens, kommer du att få nycklarna, inte licensfilen. Den här uppmätta nyckeln kan användas med klassen `Metered` speciellt introducerad för detta ändamål.

Följande kodexempel visar hur man anger mättade offentliga och privata nycklar:

```py
import aspose.threed as a3d

# Create an instance of CAD Metered class
metered = a3d.Metered()

# Access the set_metered_key property and pass public and private keys as parameters
metered.set_metered_key("*****", "*****")

# Get metered data amount before calling API
amountbefore = a3d.metered.get_consumption_quantity()
# Display information
print("Amount Consumed Before: " + str(amountbefore))

# Load the scene from disk.
scene = a3d.Scene.from_file("3D Model.fbx")
# Save as pdf
scene.save("out_pdf.pdf", a3d.FileFormat.PDF)

# Get metered data amount After calling API
amountafter = a3d.metered.get_consumption_quantity()
# Display information
print("Amount Consumed After: " + str(amountafter))
```

{{% alert color="primary" %}}

Observera att du måste ha en stabil Internetuppkoppling för korrekt användning av Metered licensen, eftersom mätaren kräver konstant interaktion med våra tjänster för korrekta beräkningar. För mer information, se avsnittet [”Meterad Licensing”](https://purchase.aspose.com/faqs/licensing/metered).

{{% /alert %}}



