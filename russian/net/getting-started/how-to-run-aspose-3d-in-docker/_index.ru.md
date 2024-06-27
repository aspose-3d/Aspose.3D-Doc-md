---
title: Как запустить Aspose.3D в Docker
type: docs
description: Запустите Aspose.3D в контейнере Docker для Linux, Windows Сервера и любой ОС.
weight: 139
url: /ru/net/how-to-run-aspose-3d-in-docker/
---
Микросервисы, в сочетании с контейнеризацией, позволяют легко комбинировать технологии. Docker позволяет легко интегрировать функциональность Aspose.3D в ваше приложение, независимо от того, какая технология находится в вашем стеке разработки.

В случае, если вы нацелены на микросервисы, или если основная технология в вашем стеке не .NET, C++ или Java, но вам нужно Aspose. функциональность 3D, или если вы уже используете Docker в своем стеке, то вы можете быть заинтересованы в использовании Aspose.3D в Docker-контейнере.

## Предпосылки

- Docker должен быть установлен в вашей системе. Для получения информации о том, как установить Docker на Windows или Mac, обратитесь к ссылкам в разделе «См. также».

- Также обратите внимание, что в приведенном ниже примере используется Visual Studio 2019, .NET Core 3,1 SDK.


## Применение

В этом примере вы создадите простое консольное приложение, которое генерирует файл 3D и сохранит его во всех поддерживаемых форматах сохранения. Затем приложение может быть построено и запущено в Docker.

### Создание консольных приложений

Чтобы создать программу, выполните следующие действия:
1. После установки Docker убедитесь, что он использует контейнеры Linux (по умолчанию). При необходимости выберите опцию Переключение на контейнеры Linux в меню Docker Desktops.
1. В Visual Studio создайте консольное приложение .NET Core.<br>
! [Для: имаге_альт_текст](create-a-new-project.png)<br>
1. Установите последнюю версию Aspose.3D с NuGet.<br>
! [Для: имаге_альт_текст](nuget-aspose-3d.png)<br>
1. Поскольку приложение будет запущено в Linux, должны быть установлены соответствующие собственные ресурсы Linux. Начните с базового образа dotnet core sdk 3,1 и установите libgdiplus libc6-dev.
1. После добавления всех необходимых зависимостей напишите простую программу, которая создаст плоскость и изменит ее ориентацию и сохранит ее во всех поддерживаемых форматах сохранения:<br>
**.NET**<br>
{{< highlight "csharp" >}}
using System;
namespace Aspose.3D.Docker
{
    class Program
    {
        static void Main(string[] args)
        {
            // Initialize scene object
            Scene scene = new Scene();

            // Set Vector
            scene.RootNode.CreateChildNode(new Plane() { Up = new Vector3(1, 1, 3) });

            //This will generate a plane that has customized orientation
            scene.Save("ChangePlaneOrientation.obj");
        }
    }
}

{{< /highlight >}}

Обратите внимание, что папка «TestOut» указана как выходная папка для сохранения выходных документов. При запуске приложения в Docker папка на хост-машине будет монтирована в эту папку в контейнере. Это позволит вам легко просмотреть вывод, сгенерированный Aspose.3D в контейнере Docker.

### Настройка Dockerfile

Следующим шагом является создание и настройка Dockerfile.

1. Создайте Dockerfile и поместите его рядом с файлом решения вашего приложения. Сохранить это имя файла без расширения (по умолчанию).
1. В Dockerfile, укажите:

{{< highlight "plain" >}}
FROM mcr.microsoft.com/dotnet/core/sdk:3.1-buster 
COPY fonts/* /usr/share/fonts/
WORKDIR /app
COPY . ./
RUN apt-get update && \
    apt-get install -y --allow-unauthenticated libgdiplus libc6-dev
RUN dotnet publish "Aspose.3D.Docker.csproj" -c Release -o /app/publish
ENTRYPOINT ["dotnet", "publish/Aspose.3D.Docker.dll"]
{{< /highlight >}}

Выше представлен простой Dockerfile, который содержит следующие инструкции:

- Образ SDK, который будет использоваться. Вот он. Изображение Net Core SDK 3,1. Docker загрузит его, когда будет запущена сборка. Версия SDK указана в виде тега.
- Команда для копирования всего в контейнер, публикации приложения и указания точки входа.
- Команда для установки libgdiplus запускается в контейнере. Это требуется для System.Drawing.Common.

### Создание и запуск приложения в Docker

Теперь приложение можно построить и запустить в Docker. Откройте вашу любимую командную строку, измените каталог на папку с приложением (папку, в которой находятся файл решения и Dockerfile) и выполните следующую команду:

{{< highlight "plain" >}}
docker build -t actest .
{{< /highlight >}}

При первом выполнении этой команды может потребоваться больше времени, так как Docker необходимо загрузить необходимые образы. Как только предыдущая команда будет завершена, выполните следующую команду:

{{< highlight "plain" >}}
docker run --mount type=bind,source=C:\Temp,target=/TestOut --rm actest from Docker
{{< /highlight >}}

{{% alert color="primary" %}} 

Обратите внимание на аргумент mount, потому что, как упоминалось ранее, папка на хост-машине монтируется в папку контейнера, чтобы легко видеть результаты выполнения приложения. Пути в Linux чувствительны к случаю.

{{% /alert %}}

## Поддержка изображений Aspose.3D

- Aspose.3D for .NET Стандарт не поддерживает EMF и TIFF в Linux.


## Больше примеров

***1. Запуск приложения в Windows Server 2019***

- Докерфайл

{{< highlight "plain" >}}
FROM microsoft/dotnet-framework:4.7.2-sdk-windowsservercore-ltsc2019
WORKDIR /app
COPY . ./
RUN dotnet publish "Aspose.3D.Docker.csproj" -c Release -o /app/publish
ENTRYPOINT ["dotnet", "publish/Aspose.3D.Docker.dll"]
{{< /highlight >}}

- Создание образа Docker

{{< highlight "plain" >}}
docker build -t actest .
{{< /highlight >}}

- Запустить образ Docker

{{< highlight "plain" >}}
docker run --mount type=bind,source=C:\Temp,target=c:\TestOut --rm actest from Docker
{{< /highlight >}}

## Смотрите также

- [Установите Docker Desktop на Windows](https://docs.docker.com/docker-for-windows/install/)
- [Установите рабочий стол Docker на Mac](https://docs.docker.com/docker-for-mac/install/)
- [Visual Studio 2019, .NET, Core 3,1 SDK](https://docs.microsoft.com/en-us/dotnet/core/install/windows?tabs=netcore31#dependencies)
- Опция [Переключиться на контейнеры Linux](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers)
- Дополнительная информация о [.NET Core SDK](https://hub.docker.com/_/microsoft-dotnet-sdk)
