---
title: Spara 3D Scene som HTML i C#
linktitle: Spara 3D Scene som HTML
type: docs
weight: 90
url: /sv/net/save-3d-scene-as-html/
---
##  **Översikt**

Den här artikeln förklarar hur du kan konvertera 3D-filer till HTML efter [Lasta in dem i sceneobjekt](https://docs.aspose.com/3d/net/create-and-read-an-existing-3d-scene/) med C# och omfattar ett brett sortiment av ämnen (beakta [Stödda filformat](https://docs.aspose.com/3d/net/supported-file-formats/)) e. g.

- Konvertera 3DS till HTML med hjälp av C#
- Konvertera FBX till HTML i C#
- Konvertera STL till HTML i C#
- Konvertera U3D till HTML i C#
- Konvertera OBJ till HTML i C#


{{% alert color="primary" %}} 

Denna funktion stöds av version 19.9 eller större.

{{% /alert %}} 
##  **Spara 3D Scene som HTML**
Aspose.3D for .NET tillhandahåller klass `Html5SaveOptions` för att spara en 3D scen som HTML. När du exporterar scenen till filen HTML5, exporterar API tre filer, en `HTML` fil, en Aspose 3DWeb- fil(*. * a3dw**), och en uppvisad `JavaScript` fil. För att bara exportera a3dw-fil kan du ange Aspose 3DWeb som exporttyp, och återanvänd JavaScript-filen inom din egen HTML sida. Följande C# kodsnippet visar hur man sparar en 3D scen som HTML.



{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-HtmlSaveOption.cs" >}}

{{% alert color="primary" %}} 

På grund av webbläsarens säkerhetsgränser kan den exporterade HTML-filen inte öppnas direkt. du måste öppna den via en webbserver, om du har python3 installerad, kan du starta webbservern i kommandoraden i den exporterade katalogen

{{% /alert %}} 

{{< highlight "java" >}}

 python3 -m http.server

{{< /highlight >}}

Öppna den då.<http://localhost:8000/test.html>. Webbens återgivning använder WebGL2, som du kan använda.<https://get.webgl.org/webgl2/>För att kontrollera om din webbläsare stöder det eller inte.


