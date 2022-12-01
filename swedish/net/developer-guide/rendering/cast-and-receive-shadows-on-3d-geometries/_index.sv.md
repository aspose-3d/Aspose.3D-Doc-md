---
title: Gjut och ta emot skuggor på 3D Geometrier
type: docs
weight: 10
url: /sv/net/cast-and-receive-shadows-on-3d-geometries/
description: Generellt kan vissa 3D filformat lagra skuggrelaterade inställningar i geometri som FBX. Med Aspose.3D for .NET, Utvecklare kan återge en bild genom att kartlägga skuggor från en ljuskällas synvinkel. Bildkvaliteten beror på ljuskällan, höjdvinkeln och avståndet mellan kameran och geometriska objekt.
---
{{% alert color="primary" %}}

Generellt kan vissa 3D filformat lagra skuggrelaterade inställningar i geometri som FBX. Användning[Aspose.3D for .NET](https://products.aspose.com/3d/net/), Kan utvecklare återge en bild genom att kartlägga skuggor från en ljuskällas synpunkt. Bildkvaliteten beror på ljuskällan, höjdvinkeln och avståndet mellan kameran och geometriska objekt.

{{% /alert %}}
## **Kasta och ta emot skugga**
Som standard kastar alla objekt i scenen skuggor från en ljuskälla. Utvecklare kan också ta emot skuggor per objekt base i objektytan. Detta kodexempel avslöjar hur ljus- och kameraobjekt ska ställas in. Den skapar också ett plan och placerar tre objekt med olika färger och skugginställningar.

Alla geometrier har `CastShadows = true` och `ReceiveShadows=true`, skuggorna av röd box och torus gjutna till planet, Den röda lådan tar inte emot skuggor och blå lådan kastar inte skuggor.
### **Programmeringsprova**
Detta kodexempel kastar och får skuggor på 3D geometries.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Rendering-CastAndReceiveShadow-CastAndReceiveShadow.cs" >}}


**Redigeringsresultat**

![TOD:imageName_Av_Text:](cast-and-receive-shadows-on-3d-geometries_1.png)
