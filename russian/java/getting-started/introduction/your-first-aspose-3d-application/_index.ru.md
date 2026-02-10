---
title: Ваша первая заявка Aspose.3D
type: docs
weight: 30
url: /ru/java/your-first-aspose-3d-application/
description: Создайте, отредактируйте и сохраните свой первый 3D-файл в любых поддерживаемых форматах, используя Aspose.3D for Java, чтобы испытать его простоту и мощь в Java.
keywords: Java , Aspose.3D for Java , The first application using Aspose.3D for Java, The first program via Aspose.3D for Java.
---
{{% alert color="primary" %}}

В этом руководстве объясняется, как создать свое первое приложение, используя Aspose.3D-это простой API. Это простое приложение создает 3d файл в указанной 3D сцене.

{{% /alert %}}

##  **Как создать приложение**

Следующие шаги создают приложение, используя Aspose.3D API:

1. Создайте экземпляр класса [Сцена](https://reference.aspose.com/3d/java/com.aspose.threed/scene/).
1. Если у вас есть лицензия, то [Применить его](/3d/ru/java/licensing/).
Если вы используете ознакомочную версию, пропустите строки кода, связанные с лицензией.
1. Создайте новый файл 3D или откройте существующий файл 3D.
1. Доступ к содержимому сцены в файле 3D.
1. Сгенерируйте измененный файл 3D.

Осуществление вышеуказанных шагов показано на примерах, приведенных ниже.

###  **Как создать документ новой сцены**

Следующий пример создает новый файл сцены 3D с нуля. Сначала создайте сцену 3D, а затем сохраните файл в формате FBX.

{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
MyDir = MyDir + "document.fbx";
// Create an object of the Scene class
Scene scene = new Scene();
// Save 3D scene document
scene.save(MyDir, FileFormat.FBX7500ASCII);
{{< /highlight >}}

###  **Как открыть существующий файл**

Следующий пример открывает существующий файл шаблона 3D с именем "document.fbx", а затем сохраняет сцену или документ 3D в потоке в различных поддерживаемых форматах 3D.

{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// Load a 3D document into Aspose.3D
Scene scene = new Scene();
// Open an existing 3D scene
scene.open(MyDir + "document.fbx");
// Save Scene to a stream
try (MemoryStream dstStream = new MemoryStream()) {
    scene.save(dstStream, FileFormat.FBX7500ASCII);
}
// Save Scene to a local path
scene.save(MyDir + "output_out.fbx", FileFormat.FBX7500ASCII);
{{< /highlight >}}
