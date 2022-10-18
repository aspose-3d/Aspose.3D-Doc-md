---
title: Render 3D scene in web page
type: docs
weight: 50
url: /net/render-3d-scene-in-web-page/
description: Using Aspose.3D for .NET, developers can render an image to view a realistic image of 3D model, with or without the enhanced background, textures, shadows and also adjust the image size.
---

{{% alert color="primary" %}}

Using [Aspose.3D for .NET](https://products.aspose.com/3d/net/), developers can convert a 3D scene into USDZ file, and visualize it in web page using Aspose.3D Web renderer.

{{% /alert %}}

## **Get the web renderer**

You can get the web renderer from our [releases](https://releases.aspose.com/3d/net/), there are 4 files in the `web-renderer` folder:

* aspose.3d-2.1.js
* aspose.3d-2.1.dat
* aspose.3d-2.1.wasm
* aspose3d.d.ts


## **Convert a scene into USDZ file**
Our web renderer supports USDZ import and export inside web browser, we need to convert a scene into USDZ before visualizing it in web browser, the code sample to convert scene into USDZ file:

```
using Aspose.ThreeD;

Scene.FromFile("input.fbx").Save("output.usdz");
```


## **Serve the file through HTTP server**

Due to browser's restrictions, all files including web renderer and the 3D file should be served through HTTP/HTTPS protocol, you can use a python command line to start a simple http server that listening on port 8000:

```
python3 -m http.server
```

## **Load the scene using JavaScript**

Create a new HTML page, and load the web renderer:

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

More information of `aspose3d` can be found in the TypeScript declaration file `aspose3d.d.ts`.
