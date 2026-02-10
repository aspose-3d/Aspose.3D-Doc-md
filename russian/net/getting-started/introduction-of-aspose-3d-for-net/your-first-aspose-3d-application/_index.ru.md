---
title: Ваша первая заявка Aspose.3D
type: docs
weight: 30
url: /ru/net/your-first-aspose-3d-application/
description: Создайте, отредактируйте и сохраните свой первый 3D-файл в любых поддерживаемых форматах, используя Aspose.3D for .NET, чтобы испытать его простоту и мощь в C#.
keywords: C# , Aspose.3D for .NET , The first application using Aspose.3D for .NET, The first program via Aspose.3D for .NET.
---
{{% alert color="primary" %}}

В этом руководстве объясняется, как создать свое первое приложение, используя Aspose.3D-это простой API. Это простое приложение создает 3d файл в указанной 3D сцене.

{{% /alert %}}

##  **Как создать приложение**

Следующие шаги создают приложение, используя Aspose.3D API:

1. Создайте экземпляр класса [Сцена](https://reference.aspose.com/3d/net/aspose.threed/scene/).
1. Если у вас есть лицензия, то [Применить его](/3d/ru/net/licensing/).
Если вы используете ознакомочную версию, пропустите строки кода, связанные с лицензией.
1. Создайте новый файл 3D или откройте существующий файл 3D.
1. Доступ к содержимому сцены в файле 3D.
1. Сгенерируйте измененный файл 3D.

Осуществление вышеуказанных шагов показано на примерах, приведенных ниже.

###  **Как создать документ новой сцены**

Следующий пример создает новый файл сцены 3D с нуля. Сначала создайте сцену 3D, а затем сохраните файл в формате FBX.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET

// Create an object of the Scene class
Scene scene = new Scene();
// Save 3D scene document
scene.Save("document.fbx");

{{< /highlight >}}

###  **Как открыть существующий файл**

Следующий пример открывает существующий файл шаблона 3D с именем "document.fbx", а затем сохраняет сцену или документ 3D в потоке в различных поддерживаемых форматах 3D.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
                        
// Load a 3D document into Aspose.3D
Scene scene = new Scene();

// Open an existing 3D scene
scene.Open("document.fbx");

// Save Scene to a stream
MemoryStream dstStream = new MemoryStream();
scene.Save(dstStream, FileFormat.FBX7500ASCII);
            
// Save Scene to a local path
scene.Save("output_out.fbx");

{{< /highlight >}}
