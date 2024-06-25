---
title: Render 3D escena en la página web
type: docs
weight: 50
url: /es/net/render-3d-scene-in-web-page/
description: Usando Aspose.3D for .NET, los desarrolladores pueden renderizar una imagen para ver una imagen realista del modelo 3D, con o sin el fondo mejorado, las texturas, las sombras y también ajustar el tamaño de la imagen.
---
{{% alert color="primary" %}}

Usando [Aspose.3D for .NET](https://products.aspose.com/3d/net/), los desarrolladores pueden convertir una escena 3D en un archivo USDZ y visualizarlo en una página web usando el renderizador web Aspose.3D.

{{% /alert %}}

##  **Obtener el renderizador web**

Puede obtener el renderizador web de nuestro [Liberaciones](https://releases.aspose.com/3d/net/), hay 4 archivos en la carpeta `web-renderer`:

* Aspose.3d-2.1.js
* Aspose.3d-2.1.dat
* Aspose.3d-2,1. wasm
* Aspose3d. d.ts


##  **Convertir una escena en un archivo USDZ**
Nuestro renderizador web admite la importación y exportación de USDZ dentro del navegador web, necesitamos convertir una escena en USDZ antes de visualizarla en el navegador web, la muestra de código para convertir la escena en un archivo USDZ:

```
using Aspose.ThreeD;

Scene.FromFile("input.fbx").Save("output.usdz");
```


##  **Servir el archivo a través del servidor HTTP**

Debido a las restricciones del navegador, todos los archivos, incluido el renderizador web y el archivo 3D, deben servirse a través del protocolo HTTP/HTTPS, puede usar una línea de comandos de python para iniciar un servidor http simple que escucha en el puerto 8000:

```
python3 -m http.server
```

##  **Cargar la escena usando JavaScript**

Cree una nueva página HTML y cargue el renderizador web:

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

Puede encontrar más información de `aspose3d` en el archivo de declaración de TypeScript `aspose3d.d.ts`.
