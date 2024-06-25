---
title: 在网页中呈现 3D 场景
type: docs
weight: 50
url: /zh/net/render-3d-scene-in-web-page/
description: 使用 Aspose.3D for .NET，开发人员可以渲染图像以查看 3D 模型的逼真图像，具有或不具有增强的背景、纹理、阴影，还可以调整图像大小。
---
{{% alert color="primary" %}}

使用 [Aspose.3D for .NET](https://products.aspose.com/3d/net/)，开发人员可以将 3D 场景转换为 USDZ 文件，并使用 Aspose.3D web渲染器在网页中将其可视化。

{{% /alert %}}

##  **获取web渲染器**

您可以从我们的 [发布](https://releases.aspose.com/3d/net/) 获取web渲染器，`web-renderer` 文件夹中有4个文件:

* aspose.3d-2.1.js
* aspose.3d-2.1.dat
* aspose.3d-2.1.wasm
* aspose3d.d.ts


##  **将场景转换为 USDZ 文件**
我们的web渲染器支持 USDZ 在web浏览器中导入和导出，我们需要在web浏览器中可视化之前将场景转换为 USDZ，将场景转换为 USDZ 文件的代码示例:

```
using Aspose.ThreeD;

Scene.FromFile("input.fbx").Save("output.usdz");
```


##  **通过HTTP服务器提供文件**

由于浏览器的限制，所有文件，包括web渲染器和 3D 文件应通过HTTP/HTTPS协议提供，您可以使用python命令行启动一个简单的http服务器，监听端口8000:

```
python3 -m http.server
```

##  **使用JavaScript加载场景**

创建一个新的 HTML 页，并加载web呈现器:

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

可以在TypeScript声明文件 `aspose3d.d.ts` 中找到 `aspose3d` 的更多信息。
