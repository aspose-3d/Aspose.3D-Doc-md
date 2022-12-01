---
title: Licensiering
description: "Aspose.3D för Python via .NET ger olika planer för köp eller erbjuder en gratis rättegång och en 30-dagars temporär Licens för utvärdering med licensierings- och prenumerationspolicy. "
type: docs
weight: 80
url: /sv/python-net/licensing/
---
Ibland, för att studera systemet bättre, du vill dyka in i koden så snabbt som möjligt. För att göra det lättare, Aspose.3D tillhandahåller olika planer för köp eller erbjuder en gratis rättegång och en 30-dagars temporär licens för utvärdering.

{{% alert color="primary" %}}

Observera att det finns ett antal allmänna policyer och praxis som vägleder dig om hur du utvärderar, licensierar och köper våra produkter. Du kan hitta dem i["Inköpspolicyer och FAQ"](https://purchase.aspose.com/policies)Sektion.

{{% /alert %}}

## **Utvärdera Aspose.3D**
Du kan enkelt ladda ner Aspose.3D för utvärdering. Utvärderingspaketet är detsamma som det köpta paketet. Utvärderingsversionen blir helt enkelt licensierad när du lägger till några rader av kod för att tillämpa licensen.

## **Utvärderingsversionsbegränsning**
Utvärderingsversionen innehåller alla funktioner utom följande:

- Användare kan endast öppna/importera högst 50 3D dokument till en Scene.
- Varje nod får inte ha mer än 5 barnnoder.
- Varje nod kan inte ha mer än 2 bifogade enheter.
- Varje geometri kan inte ha mer än 2 bifogade vertex element.
- Varje nod får inte ha mer än 1 material.
- Användare kan endast spara högst 50 3D dokument till en Scene.
- Användarna kommer också att se en utvärdering vattenstämpel i de återgivna bilderna och alla andra utdatafiler.

{{% alert color="primary" %}} 
Om du använder Aspose.3D utan rätt körkort, det skulle kunna utlösa en `aspose.threed.TrialException` när användningen nådde de olicensierade begränsningarna, kan du stänga av undantaget genom:

* [Köp en fullständig licens](https://purpose.aspose.com/buy).
* Begär en 30 dagars tillfällig licens, se [Hur får man en tillfällig licens?] (https://köp. Förmodligen. För mer information.
* Använd manuellt ett block 'försök/except' på'Scene. Open/save', detta undantag är bara en anmälan, ignorera det kommer inte att påverka laddande/sparande.

{{% /alert %}} 


## **Om licensen**
Du kan enkelt ladda ner en utvärderingsversion av Aspose.3D för Python via .NET från dess[Ladda ner sidan](https://pypi.org/project/aspose.3d/). Utvärderingsversionen ger absoluta**Samma förmågar**Som den licensierade versionen av Aspose.3D. Dessutom: utvärderingsversionen blir helt enkelt licensierad efter att du köper en licens och lägga till ett par rader av kod för att tillämpa licensen ..

Licensen är enkel text XML-fil som innehåller detaljer såsom produktnamnet, antal utvecklare den är licensierad till, prenumerationsdatum, och så vidare. Filen är digitalt signerad, så ändra inte filen. Även ett oavsiktligt tillägg av en extra radbrytning till innehållet i filen kommer att ogiltigförklara den.

För att undvika begränsningarna i samband med utvärderingsversionen måste du ställa in en licens innan du används**Aspose.3D**. Du behöver bara ställa in en licens en gång per ansökan eller process.

## Köpt licens

Efter köpet måste du tillämpa licensfilen eller strömmen. I detta avsnitt beskrivs alternativ för hur detta kan göras, och även kommentarer till vissa vanliga frågor.

{{% alert color="primary" %}}

Du måste ställa in licensen:
* Endast en gång per programdomän.
* Före användning av någon annan klass Aspose.3D

{{% /alert %}}

{{% alert color="primary" %}}

Du hittar prisuppgifter på[’Prisuppgifter’](https://purchase.aspose.com/pricing/3d/family)Sidan.

{{% /alert %}}

### **Ställa in en licens i Aspose.3D för Python via .NET**

Licenser kan tillämpas från olika platser:

* Explicit sökväg.
* Mappen som innehåller python scriptet som kallar Aspose.3D för Python via .NET
* Ström
* Som en meterad licens - en ny licens mekanism

{{% alert color="primary" %}}

Använd `set_license` metoden för att licensiera en komponent.

Att ringa `set_license` flera gånger är inte skadligt, det bara slösar processor tid.

{{% /alert %}}

I avsnitten nedan beskriver vi de två gemensamma metoderna för att ställa in licensen.

#### **Tillämpa en licens med hjälp av en fil**
Den enklaste metoden för att ställa in en licens kräver att du placerar licensfilen i samma mapp som innehåller python script som ringer 07. 6103481 för Python och ange bara filnamnet utan sökväg.

Denna kodsnutt används för att ange en licensfil:

**Python**

```py
import aspose.threed as a3d

# Instantiate an instance of license and set the license file through its path
license = a3d.License()
license.set_license("Aspose.3D.lic")
```

När du ringer `set_license` metoden, ska licensnamnet vara samma som i din licensfil. Du kan till exempel ändra licensfilnamn till "Aspose.3D.lic.xml". Sedan, i din kod, måste du skicka det nya licensnamnet (Aspose.3D.lic.xml) till SetLicense metoden.

#### **Tillämpa en licens från en ströma**
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

Aspose.3D tillåter utvecklare att applicera en uppmätta nyckel. Detta är en ny licensmekanism.

Den nya tillståndsmekanismen kommer att användas tillsammans med den befintliga tillståndsmetoden. De kunder som vill faktureras på grundval av användningen av API funktioner kan använda uppmätta licensiering.

Efter att ha slutfört alla nödvändiga steg för att få denna typ av licens, kommer du att få nycklarna, inte licensfilen. Denna uppmätta nyckel kan användas med hjälp av klassen `Metered` speciellt introducerad för detta ändamål.

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

Observera att du måste ha en stabil Internetuppkoppling för korrekt användning av Metered licensen, eftersom mätaren kräver konstant interaktion med våra tjänster för korrekta beräkningar. För ytterligare upplysningar hänvisas till:[”Meterad licensiering FAQ”](https://purchase.aspose.com/faqs/licensing/metered)Sektion.

{{% /alert %}}



