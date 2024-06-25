---
title: How to Run Aspose.3D for .Net6
type: docs
description: How to Run Aspose.3D for .Net6
weight: 138
url: /tr/net/how-to-run-aspose-3d-for-net6/
---
## Overview

Için. Net6 (veya üstü) platformları, önceki platformlarla (.netcore31 veya daha önce) karşılaştırın, önemli bir fark grafik kütüphanesi ile ilgilidir.
Bu resmi [Microsoft belge](https://learn.microsoft.com/en-gb/dotnet/core/compatibility/core-libraries/6.0/system-drawing-common-windows-only) 'da bunu açıklıyor. Net6 veya daha sonra grafik kütüphanesi "sistemini serbest bırakır. çizim. ortak" sadece Windows üzerinde desteklenecek ve grafik kütüphanesini değiştirmek için öneriler verecektir.

For Apose.3D product, we have conducted the evaluation and have completed the migration of the graphics library. We use SkiaSharp instead of System.Drawing.Common in non-Windows systems, as suggested in Microsoft's official documentation. Please note that this critical change will take effect in Aspose.3D 22.10.1 or later for .Net6.

. Netcore31 veya daha önce, uyumluluk ve kararlılık için, şu anda hala "system. drawing. common" grafik kütüphanesini kullanıyoruz.. Netcore31 veya önceki bağımlılıklar aşağıdaki gibidir:
- Sistem. çizim. ortak, 4.7.0.
- Sistem. güvenlik. kriptografi. pkcs, 5.0.1.
- Sistem. metin. kodlama. kod sayfaları, 4.7.0.

##  Run Aspose.3D for .Net6 on Windows

Önce vs2022 ile a .net6 uygulaması oluşturabilir, ardından aşağıdaki kurulum seçeneklerini seçebilirsiniz:

### nuget üzerinden yükleyin

1. Search for Aspose.3D from NuGet: [Aspose.3D for .NET NuGet Package](https://www.nuget.org/packages/Aspose.3D/). 
You can also install Aspose.3D from the Nuget package manager in VS2022.

2. "skiasharp" veya "sistem. çizim. ortak" otomatik olarak Aspose.3D 22.10.1 veya daha sonra bir bağımlılık olarak yüklenecektir. Projenizdeki "hedef os" yapılandırmasına bağlı net6 platformları.
- Set the "Target OS" to "Windows" for your project, you will use "System.Drawing.Common" as a dependency on your windows system for .Net6 project. In this configuration, the result of the drawing is closer to .netcore31 or before.
**! [Config hedef os](targetos.png)**
- "Hedef işletim sistemi" ni "hiçbiri" veya projeniz için diğer seçeneklere ayarlayın, windows sisteminize bir bağımlılık olarak "skiasharp" ı kullanacaksınız. Net6 projesi.*Lütfen "skiasharp" kullanan versiyonun yazıcı özelliğine baskıyı desteklemediğini unutmayın.*

### Msi veya dll üzerinden yükleyin

1. [Aspose.3D.msi veya dll indirin](https://releases.aspose.com/3d/net/)

2. kurulum dizinini veya dll dizinini açın, ardından aşağıdaki adım 3 veya 4'ü seçin:

3. "net6.0-windows" alt dizinini bulun, Aspose ekleyin. 3D.dll sizin. net6 uygulamanıza ekleyin. Aşağıdaki nuget paketlerini. net6 projenize manuel olarak ekleyin:
- Sistem. çizim. ortak, 4.7.0.
- Sistem. güvenlik. kriptografi. pkcs, 6.0.3.
- Sistem. metin. kodlama. kod sayfaları, 4.7.0.

Bu şekilde, windows sisteminize bir bağımlılık olarak "system. drawing. common" 'ı kullanacaksınız. Net6 projesi. Bu yapılandırmada, çizimin sonucu daha yakındır. netcore31 veya daha önce.

4. locate the "net6.0" subdirectory, add the Aspose.3D.dll in it to your .net6 application. Manually add the following nuget packages to your .net6 project:
- Skiasharp, 2.88.6.
- Sistem. güvenlik. kriptografi. pkcs, 6.0.3.
- Sistem. metin. kodlama. kod sayfaları, 4.7.0.

Bu şekilde, windows sisteminize bir bağımlılık olarak "skiasharp" kullanacaksınız. Net6 projesi.*Lütfen "skiasharp" kullanan versiyonun yazıcı özelliğine baskıyı desteklemediğini unutmayın.*
##  Run Aspose.3D for .Net6 on Linux

Windows üzerindeki kurulum yöntemine bakın, sadece linux sisteminde grafik kütüphanesi bağımlılığı olarak skiasharp'ı seçebilirsiniz.

Linux altında skiasharp doğru kullanımını sağlamak için aşağıdaki ek işlemleri yapmanız gerekir:

1. Linux sisteminizde aşağıdaki komutu çalıştırın:
```
apt-get update && apt-get install -y libfontconfig1
```
OR
```
apk update && apk add fontconfig 
```

2. nuget paketlerini ekleyin "skiasharp. nativeassets. linux 2.82.8". net6 projenize.

3. Or you can choose to add nuget packages "SkiaSharp.NativeAssets.Linux.NoDependencies 2.88.6" to your .net6 project, instead of the two steps above.

### Ubuntu için örnek dockerfile

1. nuget paketlerini ekleyin "skiasharp. na. eassets. linux 2.82.8". net6 projenize.

2. aşağıdaki dockerfile kullanın:
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

### Alp için örnek dockerfile

1. nuget paketlerini ekleyin "skiasharp. na. eassets. linux 2.82.8". net6 projenize.

2. aşağıdaki dockerfile kullanın:
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
