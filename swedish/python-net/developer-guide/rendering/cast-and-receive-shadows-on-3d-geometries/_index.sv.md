---
title: Kasta och ta emot skuggor på 3D Geometrier
type: docs
weight: 10
url: /sv/python-net/cast-and-receive-shadows-on-3d-geometries/
description: Generellt kan vissa 3D filformat lagra skuggrelaterade inställningar i geometri som FBX. Med Aspose.3D for Python via .NET kan utvecklare göra en bild genom att kartlägga skuggor från en ljuskällas synpunkt. Bildkvaliteten beror på ljuskällan, höjdvinkeln och avståndet mellan kameran och geometriska objekt.
---
{{% alert color="primary" %}}

Generellt kan vissa 3D filformat lagra skuggrelaterade inställningar i geometri som FBX. Med [Aspose.3D for Python via .NET](https://products.aspose.com/3d/python-net/) kan utvecklare göra en bild genom att kartlägga skuggor från en ljuskällas synpunkt. Bildkvaliteten beror på ljuskällan, höjdvinkeln och avståndet mellan kameran och geometriska objekt.

{{% /alert %}}
##  **Kasta och ta emot skugga**
Som standard kastar alla objekt i scenen skuggor från en ljuskälla. Utvecklare kan också ta emot skuggor per objekt base i objektytan. Detta kodexempel avslöjar hur ljus- och kameraobjekt ska ställas in. Den skapar också ett plan och placerar tre objekt med olika färger och skugginställningar.

Alla geometrier har `cast_shadows = True` och `receive_shadows = True`, skuggorna av röd ruta och torus kastade till planet, Den röda lådan tar inte emot skuggor och blå lådan kastar inte skuggor.
###  **Programmeringsprova**
Det här kodexemplet kastar och tar emot skuggor på 3D geometries.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Rendering-CastAndReceiveShadow-CastAndReceiveShadow.py" >}}


**Redigeringsresultat**

![todo:image_alt_text](cast-and-receive-shadows-on-3d-geometries_1.png)
