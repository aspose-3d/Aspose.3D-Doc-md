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



{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java
// Initialize a scene
Scene scene = new Scene();
// Initialize a node
Node node = scene.getRootNode().createChildNode(new Cylinder());
// Set child node properites
LambertMaterial mat = new LambertMaterial();
mat.setDiffuseColor(new Vector3(0.34,0.59, 0.41));
node.setMaterial(mat);
Light light = new Light();
light.setLightType(LightType.POINT);
scene.getRootNode().createChildNode(light).getTransform().setTranslation(10, 0, 10);
// Initialize HTML5SaveOptions
HTML5SaveOptions opt = new HTML5SaveOptions();
// Turn off the grid
opt.setShowGrid(false);
//Turn off the user interface
opt.setShowUI(false);
scene.save(RunExamples.getDataDir() + "html5SaveOption.html", FileFormat.HTML5);

{{< /highlight >}}

{{% alert color="primary" %}} 

Из-за ограничений безопасности браузера экспортированный файл HTML не может быть открыт напрямую, вам нужно открыть его через веб-сервер, если у вас установлен python3, вы можете запустить веб-сервер в командной строке в экспортированном каталоге

{{% /alert %}} 

{{< highlight "java" >}}

 python3 -m http.server

{{< /highlight >}}

Затем откройте его<http://localhost:8000/test.html>. Веб-рендерер использует WebGL2, вы можете использовать<https://get.webgl.org/webgl2/>Чтобы проверить, поддерживает ли ваш браузер его или нет.


