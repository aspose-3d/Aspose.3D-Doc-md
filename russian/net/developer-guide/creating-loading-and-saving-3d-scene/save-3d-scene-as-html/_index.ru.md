---
title: Сохраните сцену 3D как HTML в C#
linktitle: Сохраните сцену 3D как HTML
type: docs
weight: 90
url: /ru/net/save-3d-scene-as-html/
---
##  **Обзор**

Эта статья объясняет, как вы можете конвертировать файлы 3D в HTML после [Загрузка их в объект Scene](https://docs.aspose.com/3d/net/create-and-read-an-existing-3d-scene/), используя C#, и охватывает широкий спектр тем (учитывая [Поддерживаемые форматы файлов](https://docs.aspose.com/3d/net/supported-file-formats/)), например

- Конвертируйте 3DS в HTML, используя C#
- Конвертировать FBX в HTML в C#
- Конвертировать STL в HTML в C#
- Конвертировать U3D в HTML в C#
- Конвертировать OBJ в HTML в C#


{{% alert color="primary" %}} 

Эта функция поддерживается версией 19,9 или выше.

{{% /alert %}} 
##  **Сохраните сцену 3D как HTML**
Aspose.3D for .NET предоставляет класс `Html5SaveOptions` для сохранения сцены 3D как HTML. При экспорте сцены в файл HTML5 API экспортирует три файла: файл `HTML`, файл Aspose3DWeb (*.* a3dw **) и визуализированный файл `JavaScript`. Чтобы экспортировать только файл a3dw, вы можете указать Aspose3DWeb в качестве типа экспорта и повторно использовать файл JavaScript на своей странице HTML. Следующий фрагмент кода C# показывает, как сохранить сцену 3D как HTML.



{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize 3D scene
var scene = new Scene();
// Create a child node
var node = scene.RootNode.CreateChildNode(new Cylinder());
// Set child node properites
node.Material = new LambertMaterial() { DiffuseColor = new Vector3(Color.Chartreuse) };
scene.RootNode.CreateChildNode(new Light() { LightType = LightType.Point }).Transform.Translation = new Vector3(10, 0, 10);
// Create a Html5SaveOptions
var opt = new Html5SaveOptions();
//Turn off the grid
opt.ShowGrid = false;
//Turn off the user interface
opt.ShowUI = false; 
// Save 3D to HTML5
scene.Save("HtmlSaveOption.html", opt);

{{< /highlight >}}

{{% alert color="primary" %}} 

Из-за ограничений безопасности браузера экспортированный файл HTML не может быть открыт напрямую, вам нужно открыть его через веб-сервер, если у вас установлен python3, вы можете запустить веб-сервер в командной строке в экспортированном каталоге

{{% /alert %}} 

{{< highlight "java" >}}

 python3 -m http.server

{{< /highlight >}}

Затем откройте его<http://localhost:8000/test.html>. Веб-рендерер использует WebGL2, вы можете использовать<https://get.webgl.org/webgl2/>Чтобы проверить, поддерживает ли ваш браузер его или нет.


