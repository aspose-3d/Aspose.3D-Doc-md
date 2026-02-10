---
description: "Denna dokumentationssida demonstrerar hur man läser egenskaper från en IFC-fil med Aspose.3D för .NET."
linkTitle: IFC‑egenskapsstöd
title: "Stöd för IFC‑egenskaper"
type: docs
weight: 14
---
## Översikt

IFC Property Support är en funktion i Aspose.3D som tillåter utvecklare att läsa egenskapsuppsättningar och elementkvantiteter som definieras i IFC‑filer. Dessa egenskaper lagras i `IFCPROPERTYSET`‑ och `IFCELEMENTQUANTITY`‑entiteter och kan nås via metoden `A3DObject.GetProperty`.

## Vad är IFC Property Support?

I IFC‑schemat kan byggnadselement ha associerade egenskapsuppsättningar (`IFCPROPERTYSET`) och elementkvantiteter (`IFCELEMENTQUANTITY`). Aspose.3D mappar dessa till ett generiskt egenskapsgränssnitt, som exponeras via `A3DObject.GetProperty(string propertyName)`. Detta möjliggör hämtning av värden såsom brandklass, värmegenomgång eller materialkvantiteter direkt från 3D‑modellen.

## Varför använda IFC Property Support?

* Få tillgång till rik semantisk data utan att manuellt parsra IFC‑filen.  
* Möjliggör efterföljande processer såsom kostnadsuppskattning, efterlevnadskontroll eller dataexport.  
* Kombinera geometrisk och icke‑geometrisk information i ett enda arbetsflöde.

## Aspose.3D‑stöd

Följande C#‑exempel demonstrerar hur man läser in en IFC‑fil och hämtar en egenskap:

```csharp
using Aspose.ThreeD;

var scene = Scene.FromFile("sample.ifc");

// Hitta ett specifikt element, t.ex. en vägg
var wallNode = scene.RootNode.Children.FirstOrDefault(n => n.Name == "Wall_123");

// Hämta ett egenskapsvärde
if (wallNode != null)
{
    // Egenskapsnamn enligt definierat i IFC-filen
    var fireRating = wallNode.GetProperty("ifc:FireRating");
    Console.WriteLine($"Fire Rating: {fireRating}");

    // Exempel på elementkvantitet
    var volume = wallNode.GetProperty("ifc:GrossVolume");
    Console.WriteLine($"Gross Volume: {volume}");
}
```

### Anteckningar

* Egenskapsnamn som definieras i en IFC‑fil har prefixet `ifc:` för att undvika konflikter med inbyggda egenskaper.  
* Egenskapsnamn är skiftlägeskänsliga och måste matcha namnen som definieras i IFC‑filen.  
* `GetProperty` returnerar ett `object`; kasta till rätt typ (t.ex. `double`, `string`) vid behov.  
* Detta exempel visar hur egenskaper hämtas från `Node`; dock kan alla efterföljande klasser till `A3DObject` använda `GetProperty`.  
* Om en egenskap inte finns, returnerar `GetProperty` `null`.

## Referenser

* [Link to official Aspose.3D IFC documentation](/3d/net/supported-file-formats/ifc)  
* Länk till [`Aspose.ThreeD.A3DObject`](https://reference.aspose.com/3d/net/aspose.threed/a3dobject/)  
* IFC‑specifikationen för `IFCPROPERTYSET` och `IFCELEMENTQUANTITY`