---
title: Spara 3D scen som HTML
type: docs
weight: 90
url: /sv/python-net/save-3d-scene-as-html/
---
{{% alert color="primary" %}} 

Denna funktion stöds av version 19.9 eller större.

{{% /alert %}} 
# **Spara 3D scen som HTML**
Aspose.3D för Python via .NET ger `Html5SaveOptions` klass för att spara en 3D scen som 076143. 481. När du exporterar scenen till filen HTML5, kommer API att exportera tre filer, en fil `HTML`, en Aspose3DWeb-fil (*.**A3dw**), Och en återgiven fil 'JavaScript'. För att endast exportera a3dw-fil kan du ange Aspose3DWeb som exporttyp, och återanvänd JavaScript-filen inom din egen sida HTML. Följande kod snippet visar hur man sparar en 3D scen som HTML.



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-HtmlSaveOption.py" >}}

{{% alert color="primary" %}} 

På grund av webbläsarens säkerhetsgränser kan den exporterade HTML-filen inte öppnas direkt, du måste öppna den via en webbserver, om du har python3 installerad, kan du starta webbservern i kommandoraden i den exporterade katalogen

{{% /alert %}} 

{{< highlight "java" >}}

 python3 -m http.server

{{< /highlight >}}

Öppna den då.<http://localhost:8000/test.html>. Webbens återgivning använder WebGL2, som du kan använda.<https://get.webgl.org/webgl2/>För att kontrollera om din webbläsare stöder det eller inte.


