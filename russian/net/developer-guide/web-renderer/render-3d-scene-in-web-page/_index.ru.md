---
title: Рендеринг сцены 3D на веб-странице
type: docs
weight: 50
url: /ru/net/render-3d-scene-in-web-page/
description: Используя Aspose.3D for .NET, разработчики могут отрисовывать изображение для просмотра реалистичного изображения модели 3D с улучшенным фоном, текстурами, тенями или без них, а также настраивать размер изображения.
---
{{% alert color="primary" %}}

Используя [Aspose.3D for .NET](https://products.aspose.com/3d/net/), разработчики могут конвертировать сцену 3D в файл USDZ и визуализировать ее на веб-странице с помощью Aspose.3D веб-рендерера.

{{% /alert %}}

##  **Получить веб-рендерер**

Вы можете получить веб-рендерер из нашего [Релизы](https://releases.aspose.com/3d/net/), в папке `web-renderer` есть 4 файла:

* Aspose.3d-2.1.js
* Aspose.3d-2.1.dat
* Aspose.3d-2.1.wasm
* Aspose3d. d.ts


##  **Конвертировать сцену в файл USDZ**
Наш веб-рендерер поддерживает импорт и экспорт USDZ внутри веб-браузера, нам нужно преобразовать сцену в USDZ, прежде чем визуализировать ее в веб-браузере, образец кода для преобразования сцены в файл USDZ:

```
using Aspose.ThreeD;

Scene.FromFile("input.fbx").Save("output.usdz");
```


##  **Подавать файл через HTTP сервер**

Из-за ограничений браузера все файлы, включая веб-рендерер и файл 3D, должны обслуживаться через протокол HTTP/HTTPS, вы можете использовать командную строку python для запуска простого http-сервера, который прослушивает порт 8000:

```
python3 -m http.server
```

##  **Загрузить сцену с помощью JavaScript**

Создайте новую страницу HTML и загрузите веб-рендерер:

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

Более подробную информацию о `aspose3d` можно найти в файле объявления TypeScript `aspose3d.d.ts`.
