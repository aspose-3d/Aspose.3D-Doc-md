---
title: Сохраните сцену 3D как HTML
type: docs
weight: 70
url: /ru/nodejs-java/save-3d-scene-as-html/
description: Aspose.3D for Node.js via Java предоставляет класс ** HtmlSaveOptions ** для сохранения сцены 3D как HTML.
---
{{% alert color="primary" %}} 

Эта функция поддерживается версией 19,9 или выше.

{{% /alert %}} 
#  **Сохраните сцену 3D как HTML**
Aspose.3D for Node.js via Java предоставляет класс `HtmlSaveOptions` для сохранения сцен 3D как HTML. При экспорте сцены в файл HTML5 API будет экспортировать три файла: файл `HTML`, файл Aspose3DWeb (*.* a3dw **) и отрендеренный файл `JavaScript`. Чтобы экспортировать только файл a3dw, вы можете указать Aspose3DWeb в качестве типа экспорта и повторно использовать файл JavaScript на своей странице HTML. Следующий фрагмент кода показывает, как сохранить сцену 3D как HTML.

{{< highlight "java" >}}

// Initialize a scene
var scene = new aspose.threed.Scene();

scene.getRootNode().createChildNode(new aspose.threed.Cylinder());

var opt =new aspose.threed.Html5SaveOptions();
// Turn off the grid
opt.setShowGrid(false);
//Turn off the user interface
opt.setShowUI(false);

scene.save("html5SaveOption.html);

{{< /highlight >}}


{{% alert color="primary" %}} 

Из-за ограничений безопасности браузера экспортированный файл HTML не может быть открыт напрямую, вам нужно открыть его через веб-сервер, если у вас установлен python3, вы можете запустить веб-сервер в командной строке в экспортированном каталоге

{{% /alert %}} 

{{< highlight "java" >}}

 python3 -m http.server

{{< /highlight >}}

Затем откройте его<http://localhost:8000/test.html>. Веб-рендерер использует WebGL2, вы можете использовать<https://get.webgl.org/webgl2/>Чтобы проверить, поддерживает ли ваш браузер его или нет.


