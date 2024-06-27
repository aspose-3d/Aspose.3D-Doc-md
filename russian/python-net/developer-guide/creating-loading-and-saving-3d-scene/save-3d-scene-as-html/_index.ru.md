---
title: Сохраните сцену 3D как HTML
type: docs
weight: 90
url: /ru/python-net/save-3d-scene-as-html/
---
{{% alert color="primary" %}} 

Эта функция поддерживается версией 19,9 или выше.

{{% /alert %}} 
#  **Сохраните сцену 3D как HTML**
Aspose.3D for Python via .NET предоставляет класс `Html5SaveOptions` для сохранения сцен 3D как HTML. При экспорте сцены в файл HTML5 API будет экспортировать три файла: файл `HTML`, файл Aspose3DWeb (*.* a3dw **) и отрендеренный файл `JavaScript`. Чтобы экспортировать только файл a3dw, вы можете указать Aspose3DWeb в качестве типа экспорта и повторно использовать файл JavaScript на своей странице HTML. Следующий фрагмент кода показывает, как сохранить сцену 3D как HTML.



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-HtmlSaveOption.py" >}}

{{% alert color="primary" %}} 

Из-за ограничений безопасности браузера экспортированный файл HTML не может быть открыт напрямую, вам нужно открыть его через веб-сервер, если у вас установлен python3, вы можете запустить веб-сервер в командной строке в экспортированном каталоге

{{% /alert %}} 

{{< highlight "java" >}}

 python3 -m http.server

{{< /highlight >}}

Затем откройте его<http://localhost:8000/test.html>. Веб-рендерер использует WebGL2, вы можете использовать<https://get.webgl.org/webgl2/>Чтобы проверить, поддерживает ли ваш браузер его или нет.


