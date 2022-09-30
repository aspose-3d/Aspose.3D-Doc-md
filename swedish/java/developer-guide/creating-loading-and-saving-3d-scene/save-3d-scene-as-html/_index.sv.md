---
title: Spara 3D scen som HTML
type: docs
weight: 70
url: /sv/java/save-3d-scene-as-html/
description: Aspose.3D for Java ger **HtmlSparaOptions** klass för att spara en 3D sc HTML.
---
{{% alert color="primary" %}} 

Denna funktion stöds av version 19.9 eller större.

{{% /alert %}} 
# **Spara 3D scen som HTML**
Aspose.3D for Java ger `HtmlSaveOptions` klass för att spara en 3D scen som 076143488 1. När du exporterar scenen till filen HTML5, kommer API att exportera tre filer, en fil `HTML`, en Aspose3DWeb-fil (*.**A3dw**), Och en återgiven fil 'JavaScript'. För att endast exportera a3dw-fil kan du ange Aspose3DWeb som exporttyp, och återanvänd JavaScript-filen inom din egen sida HTML. Följande kod snippet visar hur man sparar en 3D scen som HTML.



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-loadsave-SaveOptions-html5SaveOption.java" >}}

{{% alert color="primary" %}} 

På grund av webbläsarens säkerhetsgränser kan den exporterade HTML-filen inte öppnas direkt, du måste öppna den via en webbserver, om du har python3 installerad, kan du starta webbservern i kommandoraden i den exporterade katalogen

{{% /alert %}} 

{{< highlight "java" >}}

 python3 -m http.server

{{< /highlight >}}

Öppna den då.<http://localhost:8000/test.html>. Webbens återgivning använder WebGL2, som du kan använda.<https://get.webgl.org/webgl2/>För att kontrollera om din webbläsare stöder det eller inte.


