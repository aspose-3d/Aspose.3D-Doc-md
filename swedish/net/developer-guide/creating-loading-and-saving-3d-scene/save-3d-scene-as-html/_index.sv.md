---
title: Spara 3D scen som HTML i C#
linktitle: Spara 3D scen som HTML
type: docs
weight: 90
url: /sv/net/save-3d-scene-as-html/
---
## **Översikt**

Denna artikel förklarar hur du kan konvertera 3D filer till HTML efter HTML[Lasta in dem i sceneobjekt](https://docs.aspose.com/3d/net/create-and-read-an-existing-3d-scene/)C# och omfattar ett brett spektrum av ämnen (beaktad)[Stödda filformat](https://docs.aspose.com/3d/net/supported-file-formats/)) T.ex.

- Konvertera 3DS till HTML med C#
- Konvertera FBX till HTML i C#
- Konvertera STL till HTML i C#
- Konvertera U3D till HTML i C#
- Konvertera OBJ till HTML i C#


{{% alert color="primary" %}} 

Denna funktion stöds av version 19.9 eller större.

{{% /alert %}} 
## **Spara 3D scen som HTML**
Aspose.3D for .NET ger `Html5SaveOptions` klass för att spara en 3D scen som 076143488 1. När du exporterar scenen till filen HTML5, kommer API att exportera tre filer, en fil `HTML`, en Aspose3DWeb-fil (*.**A3dw**), Och en återgiven fil 'JavaScript'. För att endast exportera a3dw-fil kan du ange Aspose3DWeb som exporttyp, och återanvänd JavaScript-filen inom din egen sida HTML. Följande C# kodsnippet visar hur man sparar en 3D scen som HTML.



{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-HtmlSaveOption.cs" >}}

{{% alert color="primary" %}} 

På grund av webbläsarens säkerhetsgränser kan den exporterade HTML-filen inte öppnas direkt, du måste öppna den via en webbserver, om du har python3 installerad, kan du starta webbservern i kommandoraden i den exporterade katalogen

{{% /alert %}} 

{{< highlight "java" >}}

 python3 -m http.server

{{< /highlight >}}

Öppna den då.<http://localhost:8000/test.html>. Webbens återgivning använder WebGL2, som du kan använda.<https://get.webgl.org/webgl2/>För att kontrollera om din webbläsare stöder det eller inte.


