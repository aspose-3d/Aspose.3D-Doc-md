---
title: Rendern 3D Szene auf Webseite
type: docs
weight: 50
url: /de/net/render-3d-scene-in-web-page/
description: Mit Aspose.3D for .NET können Entwickler ein Bild rendern, um ein realistisches Bild des 3D-Modells mit oder ohne erweiterten Hintergrund, Texturen und Schatten anzuzeigen und auch die Bildgröße anzupassen.
---
{{% alert color="primary" %}}

Mit [Aspose.3D for .NET](https://products.aspose.com/3d/net/) können Entwickler eine 3D-Szene in USDZ-Datei konvertieren und sie auf der Webseite mit Aspose.3D Web-Renderer visual isieren.

{{% /alert %}}

##  **Holen Sie sich den Web-Renderer**

Sie können den Web-Renderer von unseren [Releases](https://releases.aspose.com/3d/net/) erhalten, es gibt 4 Dateien im Ordner `web-renderer`:

* Assose.3d-2.1.js
* Assose.3d-2.1.dat
* Assose.3d-2.1.wasm
* Assose3d. d.ts


##  **Konvertieren Sie eine Szene in USDZ-Datei**
Unser Web-Renderer unterstützt den Import und Export von USDZ im Webbrowser. Wir müssen eine Szene in USDZ konvertieren, bevor wir sie im Webbrowser visual isieren, das Code beispiel, um die Szene in eine USDZ-Datei zu konvertieren:

```
using Aspose.ThreeD;

Scene.FromFile("input.fbx").Save("output.usdz");
```


##  **Servieren Sie die Datei über den HTTP-Server**

Aufgrund der Einschränkungen des Browsers sollten alle Dateien, einschl ießlich des Web-Renderers und der 3D-Datei, über das HTTP/HTTPS-Protokoll bereit gestellt werden. Sie können eine Python-Befehlszeile verwenden, um einen einfachen http-Server zu starten, der auf Port 8000 zuhört:

```
python3 -m http.server
```

##  **Laden Sie die Szene mit JavaScript**

Erstellen Sie eine neue HTML-Seite, und laden Sie den Web-Renderer:

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

Weitere Informationen zu `aspose3d` finden Sie in der TypeScript-Deklaration datei `aspose3d.d.ts`.
