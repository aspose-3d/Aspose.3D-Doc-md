---
title: Rendre la scène 3D dans la page Web
type: docs
weight: 50
url: /fr/net/render-3d-scene-in-web-page/
description: En utilisant Aspose.3D for .NET, les développeurs peuvent rendre une image pour afficher une image réaliste du modèle 3D, avec ou sans l'arrière-plan, les textures, les ombres améliorés et également ajuster la taille de l'image.
---
{{% alert color="primary" %}}

En utilisant [Aspose.3D for .NET](https://products.aspose.com/3d/net/), les développeurs peuvent convertir une scène 3D en fichier USDZ et la visualiser dans une page Web à l'aide du moteur de rendu Web Aspose.3D.

{{% /alert %}}

##  **Obtenez le moteur de rendu Web**

Vous pouvez obtenir le moteur de rendu Web à partir de notre [Les libérations](https://releases.aspose.com/3d/net/), il y a 4 fichiers dans le dossier `web-renderer`:

* Aspose.3d-2.1.js
* Aspose.3d-2.1.dat
* Aspose.3d-2.1.wasm
* Aspose3d. d.ts


##  **Convertir une scène en fichier USDZ**
Notre moteur de rendu Web prend en charge l'importation et l'exportation de USDZ dans le navigateur Web, nous devons convertir une scène en USDZ avant de la visualiser dans le navigateur Web, l'exemple de code pour convertir la scène en fichier USDZ:

```
using Aspose.ThreeD;

Scene.FromFile("input.fbx").Save("output.usdz");
```


##  **Servir le fichier via le serveur HTTP**

En raison des restrictions du navigateur, tous les fichiers, y compris le rendu Web et le fichier 3D, doivent être servis via le protocole HTTP/HTTPS, vous pouvez utiliser une ligne de commande python pour démarrer un serveur http simple qui écoute sur le port 8000:

```
python3 -m http.server
```

##  **Charger la scène en utilisant JavaScript**

Créez une nouvelle page HTML et chargez le moteur de rendu Web:

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

Plus d'informations sur `aspose3d` peuvent être trouvées dans le fichier de déclaration TypeScript `aspose3d.d.ts`.
