---
title: Сохранить 3D сцена как HTML в C#
linktitle: Сохранить 3D Сцена как HTML
type: docs
weight: 90
url: /ru/net/save-3d-scene-as-html/
---
## **Обзор**

Эта статья объясняет, как вы можете конвертировать файлы 3D в HTML после[Загрузка их в объект Scene](https://docs.aspose.com/3d/net/create-and-read-an-existing-3d-scene/)С использованием C# и охватывает широкий круг тем (с учетом[Поддерживаемые форматы файлов](https://docs.aspose.com/3d/net/supported-file-formats/)) Например

- Конвертировать 3DS в HTML с использованием C#
- Конвертировать FBX в HTML в C#
- Конвертировать STL в HTML в C#
- Конвертировать U3D в HTML в C#
- Конвертировать OBJ в HTML в C#


{{% alert color="primary" %}} 

Эта функция поддерживается версией 19,9 или выше.

{{% /alert %}} 
## **Сохранить 3D Сцена как HTML**
Aspose.3D for .NET предоставляет класс `Html5SaveOptions` для сохранения сцены 3D как HTML. При экспорте сцены в файл HTML5, API будет экспортировать три файла, файл `HTML`, файл Aspose3DWeb (*.**А3дв**) И отображенный файл JavaScript. Чтобы экспортировать только файл a3dw, вы можете указать Aspose3DWeb в качестве типа экспорта и повторно использовать файл JavaScript на своей странице HTML. Следующий фрагмент кода C# показывает, как сохранить сцену 3D как HTML.



{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-SaveOptions-HtmlSaveOption.cs" >}}

{{% alert color="primary" %}} 

Из-за ограничений безопасности браузера экспортированный файл HTML не может быть открыт напрямую, его нужно открыть через веб-сервер, если у вас установлен python3, вы можете запустить веб-сервер в командной строке в экспортированном каталоге

{{% /alert %}} 

{{< highlight "java" >}}

 python3 -m http.server

{{< /highlight >}}

Затем откройте его<http://localhost:8000/test.html>. Веб-рендерер использует WebGL2, вы можете использовать<https://get.webgl.org/webgl2/>Чтобы проверить, поддерживает ли ваш браузер его или нет.


