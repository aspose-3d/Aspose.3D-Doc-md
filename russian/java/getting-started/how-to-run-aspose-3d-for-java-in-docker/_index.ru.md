---
title: Как запустить Aspose.3D for Java в Docker
type: docs
description: Запустите Aspose.3D for Java в Docker-контейнере для Linux.
weight: 139
url: /ru/java/how-to-run-aspose-3d-in-docker/
---
Микросервисы, в сочетании с контейнеризацией, позволяют легко комбинировать технологии. Docker позволяет легко интегрировать функциональность Aspose.3D в ваше приложение, независимо от того, какая технология находится в вашем стеке разработки.

В случае, если вы нацелены на микросервисы, или если основная технология в вашем стеке не .NET, C++ или Java, но вам нужно Aspose. функциональность 3D, или если вы уже используете Docker в своем стеке, то вы можете быть заинтересованы в использовании Aspose.3D for Java в Docker-контейнере.

## Предпосылки

- Docker должен быть установлен в вашей системе.

## Создать приложение Java

В этом примере вы создаете приложение Java, которое создает простой 3D-файл, сохраняет его и читает. Затем приложение может быть построено и запущено в Docker.

### Создание приложения Java

Создайте приложение Java в Eclipse, используя следующий код. В этом примере мы используем Aspose.3D for Java, чтобы создать плоскость в 3d сцене и установить вектор, а затем сохранить его в формате obj.

{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// Initialize Scene
Scene scene = new Scene();
// Initialize Plane
Plane plane = new Plane();
// Set Vector
plane.setUp(new Vector3(1, 1, 3));
scene.getRootNode().createChildNode(plane);
//This will generate a plane that has customized orientation
scene.save(MyDir+"ChangePlaneOrientation.obj", FileFormat.WAVEFRONTOBJ);

{{< /highlight >}}

### Превращаем приложение Java в пакет jar

На следующем рисунке показан способ создания пакета jar с помощью меню "Экспорт" в Eclipse.

**! [Сделать Jar с помощью Eclipse(MakeJar.png)**

Теперь, когда мы написали программу Java, используя Aspose.3D for Java, мы получили пакет jar. Затем мы сделаем досье.

### Настройка Dockerfile

Следующим шагом является создание и настройка Dockerfile.

1. Создайте Dockerfile и поместите его рядом с пакетом jar. Сохранить это имя файла без расширения (по умолчанию).
2. В Dockerfile, укажите:

{{< highlight "plain" >}}
   FROM williamyeh/java8:latest

   VOLUME /tmp

   ADD TestDocker.jar app.jar

   ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom","-jar","/app.jar"]
{{< /highlight >}}

### Создание и запуск приложения в Docker

Теперь приложение можно построить и запустить в Docker. Откройте вашу любимую командную строку, измените каталог на папку с Dockerfile и выполните следующую команду:

{{< highlight "plain" >}}
docker build -t java-app .
{{< /highlight >}}

После выполнения приведенной выше команды, вы получите вывод файла 3D. На данный момент программа Java была успешно запущена в Linux Docker.
