---
title: Save 3D cene cene as HTML
type: docs
weight: 90
url: /tr/python-net/save-3d-scene-as-html/
---
{{% alert color="primary" %}} 

This özelliği 19.9 veya daha büyük sürümle desteklenir.

{{% /alert %}} 
# **Save 3D cene cene as HTML**
Python via .NET için Aspose.3D, `Html5SaveOptions` olarak 3D sahnesini kaydetmek için `Html5SaveOptions` sınıfı sağlar. Sahne 076481 481 dosyasına ihraç ederseniz, API üç dosya, bir `HTML` dosyası, bir 070734813 Deb eb dosyası (*.**A3dw**) Ve işlenmiş bir 'Javaavacript' dosyası. A3n sipariş sadece a3dw dosyasını ihraç etmek için, Aspose3 Deb eb ihracat türü olarak belirtebilir ve kendi HTML sayfanızda Javacricript dosyasını yeniden kullanabilirsiniz. Kod parçacığını takip eden T, HTML olarak 3D sahnesini nasıl kurtaracağını gösterir.



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-HtmlSaveOption.py" >}}

{{% alert color="primary" %}} 

Tarayıcının güvenlik sınırlarına Due, ihraç edilen HTML dosyası doğrudan açılamıyor, bir web sunucusu üzerinden açmanız gerekiyor, eğer python3 yüklü ise, web sunucusunu ihraç edilen dizinde komut satırına başlatabilirsiniz

{{% /alert %}} 

{{< highlight "java" >}}

 python3 -m http.server

{{< /highlight >}}

Then aç<http://localhost:8000/test.html>. The web renderer WebGL2 kullanır, kullanabilirsiniz<https://get.webgl.org/webgl2/>Tarayıcınızın destekleyip desteklemediğini kontrol etmek için.


