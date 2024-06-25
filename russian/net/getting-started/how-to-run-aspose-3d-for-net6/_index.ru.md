---
title: Как запустить Aspose.3D для. Нет6
type: docs
description: Как запустить Aspose.3D для. Нет6
weight: 138
url: /ru/net/how-to-run-aspose-3d-for-net6/
---
## Обзор

Для. Платформы NET6 (или более поздние), по сравнению с предыдущими платформами (.netcore31 или ранее), важное отличие заключается в графической библиотеке.
В этом официальном [Microsoft документа](https://learn.microsoft.com/en-gb/dotnet/core/compatibility/core-libraries/6.0/system-drawing-common-windows-only), это объясняет для. NET6 или более поздняя выпускает графическую библиотеку "System.Drawing.Common", которая будет поддерживаться только на Windows, и дает рекомендации по замене графической библиотеки.

Для продукта Apose.3D мы провели оценку и завершили миграцию графической библиотеки. Мы используем SkiaSharp вместо System.Drawing.Common в системах, не относящихся к Windows, как предлагается в официальной документации Microsoft. Обратите внимание, что это критическое изменение вступит в силу в Aspose.3D 22.10.1 или позже. Нет6.

Для. netcore31 или ранее, для совместимости и стабильности, в настоящее время мы по-прежнему используем графическую библиотеку "System.Drawing.Common". Зависимости для. netcore31 или до него следующие:
- Система. Чертеж. Общий, 4.7.0.
- Система. Безопасность. Криптография. Pkcs, 5.0.1.
- Система. Текст. Кодировка. CodePages, 4.7.0.

## Запустите Aspose.3D для. Net6 на Windows

Сначала вы можете создать приложение. net6 с помощью VS2022, затем вы можете выбрать следующие варианты установки:

### Установить через nuget

1. Найдите Aspose.3D в NuGet: [Aspose. пакет 3D for .NET NuGet](https://www.nuget.org/packages/Aspose.3D/).
Вы также можете установить Aspose.3D из менеджера пакетов Nuget в VS2022.

2. "SkiaSharp" или "System.Drawing.Common" будут установлены автоматически как зависимость Aspose.3D 22.10.1 или более поздней версии. Платформы Net6, которые зависят от конфигурации "Target OS" в вашем проекте.
- Установите "Target OS" на "Windows" для вашего проекта, вы будете использовать "System.Drawing.Common" в качестве зависимости от вашей системы Windows для. Проект Net6. В этой конфигурации результат чертежа ближе к. netcore31 или ранее.
**! [Настройка целевого объекта OS](TargetOS.png)**
- Установите «Target OS» на «Нет» или другие параметры для вашего проекта, вы будете использовать «SkiaSharp» в качестве зависимости от вашей системы Windows для. Проект Net6.*Обратите внимание, что версия, использующая "SkiaSharp" в качестве зависимости, не поддерживает функцию печати на принтере.*

### Установка через MSI или DLL

1. [Скачать Aspose.3D.msi или DLL](https://releases.aspose.com/3d/net/)

2. Откройте каталог установки или каталог DLL, затем выберите шаг 3 или 4 ниже:

3. найдите подкаталог "net6.0-windows", добавьте в него Aspose.3D.dll в ваше приложение. net6. Добавьте вручную следующие пакеты nuget в свой проект. net6:
- Система. Чертеж. Общий, 4.7.0.
- Система. Безопасность. Криптография. Pkcs, 6.0.3.
- Система. Текст. Кодировка. CodePages, 4.7.0.

Таким образом, вы будете использовать "System.Drawing.Common" в качестве зависимости от вашей системы Windows для. Проект Net6. В этой конфигурации результат чертежа ближе к. netcore31 или ранее.

4. найдите подкаталог "net6.0", добавьте в него Aspose.3D.dll в ваше приложение. net6. Добавьте вручную следующие пакеты nuget в свой проект. net6:
- SkiaSharp, 2886.
- Система. Безопасность. Криптография. Pkcs, 6.0.3.
- Система. Текст. Кодировка. CodePages, 4.7.0.

Таким образом, вы будете использовать «SkiaSharp» в качестве зависимости от вашей системы Windows для. Проект Net6.*Обратите внимание, что версия, использующая "SkiaSharp" в качестве зависимости, не поддерживает функцию печати на принтере.*
## Запустите Aspose.3D для. Net6 на Linux

Обратитесь к методу установки на Windows, вы можете выбрать только SkiaSharp в качестве зависимости от графической библиотеки в системе Linux.

Для обеспечения правильного использования SkiaSharp под Linux необходимо выполнить следующие дополнительные операции:

1. Выполните следующую команду в вашей системе Linux:
```
apt-get update && apt-get install -y libfontconfig1
```
OR
```
apk update && apk add fontconfig 
```

2. Добавьте nuget пакеты "SkiaSharp.NativeAssets.Linux 2.88.6" в свой проект. net6.

3. Или вы можете добавить nuget пакеты "SkiaSharp.NativeAssets.Linux.NoDependencies 2.88.6" в ваш проект. net6 вместо двух шагов выше.

### Пример Dockerfile для Ubuntu

1. Добавьте nuget пакеты "SkiaSharp.NativeAssets.Linux 2.88.6" в свой проект. net6.

2. Используйте следующий Dockerfile:
{{< highlight "plain" >}}
#  Ubuntu 20.04
FROM mcr.microsoft.com/dotnet/runtime:6.0-focal AS base
WORKDIR /app

#  add "libfontconfig1" package if using "SkiaSharp.NativeAssets.Linux" in your project
#  Or you need to use "SkiaSharp.NativeAssets.Linux.NoDependencies" in your project
RUN apt-get update && apt-get install -y libfontconfig1

#  Copy fonts from local to docker
#  For example, put a "fonts" folder in your project folder, and put the font files in it,
#  then, use the following line:
COPY fonts/ /usr/share/fonts

FROM mcr.microsoft.com/dotnet/sdk:6.0-focal AS build
WORKDIR /src
COPY ["Ubuntu_Docker.csproj", "."]
RUN dotnet restore "./Ubuntu_Docker.csproj"
COPY . .
WORKDIR "/src/."
RUN dotnet build "Ubuntu_Docker.csproj" -c Release -o /app/build

FROM build AS publish
RUN dotnet publish "Ubuntu_Docker.csproj" -c Release -o /app/publish

FROM base AS final
WORKDIR /app
COPY --from=publish /app/publish .
ENTRYPOINT ["dotnet", "Ubuntu_Docker.dll"]
{{< /highlight >}}

### Пример Dockerfile для Alpine

1. Добавьте nuget пакеты "SkiaSharp.NativeAssets.Linux 2.88.6" в свой проект. net6.

2. Используйте следующий Dockerfile:
{{< highlight "plain" >}}
# Alpine 3.16
FROM mcr.microsoft.com/dotnet/runtime:6.0-alpine3.16 AS base
WORKDIR /app

#  add "fontconfig" package if using "SkiaSharp.NativeAssets.Linux" in your project
#  Or you need to use "SkiaSharp.NativeAssets.Linux.NoDependencies" in your project
RUN apk update && apk add fontconfig 

#  Copy fonts from local to docker
#  For example, put a "fonts" folder in your project folder, and put the font files in it,
#  then, use the following line:
COPY fonts/ /usr/share/fonts

FROM mcr.microsoft.com/dotnet/sdk:6.0-alpine3.16 AS build
WORKDIR /src
COPY ["Alpine_Docker.csproj", "."]
RUN dotnet restore "./Alpine_Docker.csproj"
COPY . .
WORKDIR "/src/."
RUN dotnet build "Alpine_Docker.csproj" -c Release -o /app/build

FROM build AS publish
RUN dotnet publish "Alpine_Docker.csproj" -c Release -o /app/publish

FROM base AS final
WORKDIR /app
COPY --from=publish /app/publish .
ENTRYPOINT ["dotnet", "Alpine_Docker.dll"]
{{< /highlight >}}
