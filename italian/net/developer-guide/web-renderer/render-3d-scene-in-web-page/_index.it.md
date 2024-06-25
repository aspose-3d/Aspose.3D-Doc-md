---
title: Render 3D scena nella pagina web
type: docs
weight: 50
url: /it/net/render-3d-scene-in-web-page/
description: Utilizzando Aspose.3D for .NET, gli sviluppatori possono eseguire il rendering di un'immagine per visualizzare un'immagine realistica del modello 3D, con o senza lo sfondo, le trame e le ombre migliorate e anche regolare le dimensioni dell'immagine.
---
{{% alert color="primary" %}}

Utilizzando [Aspose.3D for .NET](https://products.aspose.com/3d/net/), gli sviluppatori possono convertire una scena 3D in file USDZ e visualizzarla nella pagina web utilizzando Aspose.3D Renderer Web.

{{% /alert %}}

##  **Ottieni il renderer web**

Puoi ottenere il renderer web dal nostro [Releases](https://releases.aspose.com/3d/net/), ci sono 4 file nella cartella `web-renderer`:

* Aspose.3d-2.1.js
* Aspose.3d-2.1.dat
* Aspose.3d-2.1.wasm
* Aspose3d. d.ts


##  **Convertire una scena in file USDZ**
Il nostro renderer Web supporta USDZ di importazione ed esportazione all'interno del browser Web, dobbiamo convertire una scena in USDZ prima di visualizzarla nel browser Web, il codice di esempio per convertire la scena in USDZ file:

```
using Aspose.ThreeD;

Scene.FromFile("input.fbx").Save("output.usdz");
```


##  **Servire il file tramite il server HTTP**

A causa delle restrizioni del browser, tutti i file, incluso il renderer Web e il file 3D, devono essere serviti tramite il protocollo HTTP/HTTPS, è possibile utilizzare una riga di comando python per avviare un semplice server http che ascolta sulla porta 8000:

```
python3 -m http.server
```

##  **Caricare la scena usando JavaScript**

Crea una nuova pagina HTML e carica il renderer web:

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

Ulteriori informazioni di `aspose3d` sono disponibili nel file di dichiarazione TypeScript `aspose3d.d.ts`.
