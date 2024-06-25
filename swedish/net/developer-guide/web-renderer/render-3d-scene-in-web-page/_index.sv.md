---
title: Redigera 3D scen på webbsida
type: docs
weight: 50
url: /sv/net/render-3d-scene-in-web-page/
description: Använder Aspose. 3D for .NET, kan utvecklare göra en bild för att visa en realistisk bild av 3D-modell, med eller utan den förbättrade bakgrunden, texturer, skuggor och även justera bildstorleken.
---
{{% alert color="primary" %}}

Genom att använda [Aspose.3D for .NET](https://products.aspose.com/3d/net/) kan utvecklare konvertera en 3D scen till USDZ fil, och visualisera det på webbsidan med Aspose. 3D

{{% /alert %}}

##  **Hämta webbirändaren**

Du kan hämta webbhotell från vår [Utgivningar](https://releases.aspose.com/3d/net/), det finns 4 filer i `web-renderer`-mappen:

* Aspose.3d-2.1.js
* Aspose.3d-2.1.dat.
* Aspose.3d-2.1.wasm
* Aspose3d.d.ts


##  **Konvertera en scen till USDZ-fil.**
Vår webben renderare stöder USDZ import och export inuti webbläsaren, vi måste konvertera en scen till USDZ innan vi visualiserar den i webbläsare, Kodprovet för att konvertera scen till filen USDZ:

```
using Aspose.ThreeD;

Scene.FromFile("input.fbx").Save("output.usdz");
```


##  **Servera filen via HTTP- servern**

På grund av webbläsarens begränsningar ska alla filer, inklusive webprenör och 3D-filen serveras via HTTP/HTTPS-protokollet, du kan använda en python kommandorad för att starta en enkel http-server som lyssnar på port 8000:

```
python3 -m http.server
```

##  **Ladda scenen med JavaScript.**

Skapa en ny sida med HTML och ladda webbhotell:

```
<!DOCTYPE html>
<html>
    <head>
        <title>Aspose.3D Web Renderer</title>
        <script src="aspose.3d-2.1.js"></script>
    <style>
        #canvas{width:600px;height:400px;}
    </style>

    </head>
    <body>
        <h1>Aspose.3D Web Renderer</h1>
        <canvas id='canvas'></canvas>
        <script>
            aspose3d({canvas : 'canvas', url : 'test.usdz'});
        </script>
    </body>
</html>
```

Mer information om `aspose3d` finns i TypeScript-deklarationsfilen `aspose3d.d.ts`.
