---
title: Сохраните сцену 3D как HTML
type: docs
weight: 70
url: /ru/java/save-3d-scene-as-html/
description: Aspose.3D for Java предоставляет класс ** HtmlSaveOptions ** для сохранения сцены 3D как HTML.
---
{{% alert color="primary" %}} 

Эта функция поддерживается версией 19,9 или выше.

{{% /alert %}} 
#  **Сохраните сцену 3D как HTML**
Aspose.3D for Java предоставляет класс `HtmlSaveOptions` для сохранения сцены 3D как HTML. При экспорте сцены в файл HTML5 API экспортирует три файла: файл `HTML`, файл Aspose3DWeb (*.* a3dw **) и визуализированный файл `JavaScript`. Чтобы экспортировать только файл a3dw, вы можете указать Aspose3DWeb в качестве типа экспорта и повторно использовать файл JavaScript на своей странице HTML. Следующий фрагмент кода показывает, как сохранить сцену 3D как HTML.



{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-loadsave-SaveOptions-html5SaveOption.java" >}}

{{% alert color="primary" %}} 

Из-за ограничений безопасности браузера экспортированный файл HTML не может быть открыт напрямую, вам нужно открыть его через веб-сервер, если у вас установлен python3, вы можете запустить веб-сервер в командной строке в экспортированном каталоге

{{% /alert %}} 

{{< highlight "java" >}}

 python3 -m http.server

{{< /highlight >}}

Затем откройте его<http://localhost:8000/test.html>. Веб-рендерер использует WebGL2, вы можете использовать<https://get.webgl.org/webgl2/>Чтобы проверить, поддерживает ли ваш браузер его или нет.


