---
title: Web sayfasında 3D sahne render
type: docs
weight: 50
url: /tr/net/render-3d-scene-in-web-page/
description: Aspose.3D for .NET kullanarak, geliştiriciler gelişmiş arka plan, dokular, gölgeler ile veya olmadan 3D modelinin gerçekçi bir görüntüsünü görüntülemek ve aynı zamanda görüntü boyutunu ayarlamak için bir görüntü oluşturabilirler.
---
{{% alert color="primary" %}}

Using [Aspose.3D for .NET](https://products.aspose.com/3d/net/), developers can convert a 3D scene into USDZ file, and visualize it in web page using Aspose.3D Web renderer.

{{% /alert %}}

##  **Web renderer alın**

Web renderer'ı [Bültenler](https://releases.aspose.com/3d/net/) 'dan alabilirsiniz, `web-renderer` klasöründe 4 dosya var:

* Aspose.3d-2.1.js
* Aspose.3d-2.1.dat
* Aspose.3d-2.1.wasm
* Aspose3d. d.ts


##  **Bir sahneyi USDZ dosyasına dönüştürün**
Web renderer, web tarayıcısında USDZ içe aktarma ve dışa aktarma işlemini destekliyor, web tarayıcısında görselleştirmeden önce bir sahneyi USDZ olarak dönüştürmemiz gerekiyor, kod örneği USDZ dosyasına dönüştürmek için:

```
using Aspose.ThreeD;

Scene.FromFile("input.fbx").Save("output.usdz");
```


##  **Dosyayı http sunucusu üzerinden sunun**

Tarayıcının kısıtlamaları nedeniyle, web renderer ve 3D dosyası dahil olmak üzere tüm dosyalar http/https protokolü üzerinden sunulmalıdır, 8000 bağlantı noktasında dinleyen basit bir http sunucusu başlatmak için bir python komut satırı kullanabilirsiniz:

```
python3 -m http.server
```

##  **Javascript kullanarak sahneyi yükleyin**

Yeni bir HTML sayfası oluşturun ve web işlemcisini yükleyin:

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

`aspose3d` hakkında daha fazla bilgi, typescript beyannamesi dosyasında `aspose3d.d.ts` bulunabilir.
