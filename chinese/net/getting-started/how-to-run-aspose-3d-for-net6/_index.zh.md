---
title: 如何为运行 Aspose.3D。Net6
type: docs
description: 如何为运行 Aspose.3D。Net6
weight: 138
url: /zh/net/how-to-run-aspose-3d-for-net6/
---
## 概述

为了。NET6 (或更高版本) 平台，与以前的平台 (.netcore31或之前) 相比，一个重要的区别是图形库。
在这个官方的 [Microsoft 文档](https://learn.microsoft.com/en-gb/dotnet/core/compatibility/core-libraries/6.0/system-drawing-common-windows-only) 中，它解释了。NET6或更高版本发布的图形库 “System.Drawing.Common” 将仅在 Windows 上受支持，并给出替换图形库的建议。

对于Apose.3D 产品，我们已经进行了评估并完成了图形库的迁移。我们使用SkiaSharp而不是System.Drawing.Common在非 Windows 系统中，正如 Microsoft 的官方文档所建议的那样。请注意，此关键更改将在的 Aspose.3D 22.10.1或更高版本中生效。Net6。

为。netcore31或之前，为了兼容性和稳定性，目前我们仍然使用 “System.Drawing.Common” 图形库。的依赖项。netcore31或之前的版本如下:
- System.Drawing.Common，4.7.0。
- System.Security.Cryptography.Pkcs，5.0.1。
- System.Text.Encoding.CodePages，4.7.0。

## 运行的 Aspose.3D。Windows 上的Net6

首先，你可以创建一个。net6应用程序与VS2022，那么你可以选择以下安装选项:

### 通过 nuget 安装

1. 从 NuGet 搜索 Aspose。3D: [Aspose.3D for .NET NuGet 包](https://www.nuget.org/packages/Aspose.3D/)。
您还可以从vs2022中的 Nuget 包管理器安装 Aspose.3D。

2.“SkiaSharp” 或 “System.Drawing.Common” 将作为的 Aspose.3D 22.10.1或更高版本的依赖项自动安装。Net6平台，这取决于项目中的 “目标操作系统” 配置。
- 将项目的 “目标操作系统” 设置为 “Windows”，您将使用 “System.Drawing.Common” 作为windows系统上的依赖项。Net6项目。在这种配置中，绘图的结果更接近。netcore31或之前。
**![配置目标OS](TargetOS.png)**
- 将 “目标操作系统” 设置为 “无” 或项目的其他选项，您将使用 “SkiaSharp” 作为windows系统上的依赖项。Net6项目。*请注意，使用 “SkiaSharp” 作为依赖项的版本不支持打印到打印机功能。*

### 通过msi或DLL安装

1. [下载 Aspose.3D.msi或DLL](https://releases.aspose.com/3d/net/)

2.打开安装目录或DLL目录，然后选择下面的步骤3或4:

3.找到 “net6.0-windows” 子目录，将其中的 Aspose.3D.dll添加到.net6应用程序。手动将以下 nuget 包添加到。net6项目:
- System.Drawing.Common，4.7.0。
- System.Security.Cryptography.Pkcs，6.0.3。
- System.Text.Encoding.CodePages，4.7.0。

这样，您将使用 “System.Drawing.Common” 作为windows系统的依赖项。Net6项目。在这种配置中，绘图的结果更接近。netcore31或之前。

4.找到 “net6.0” 子目录，将其中的 Aspose.3D.dll添加到.net6应用程序。手动将以下 nuget 包添加到。net6项目:
- 斯基沙尔，2.88.6。
- System.Security.Cryptography.Pkcs，6.0.3。
- System.Text.Encoding.CodePages，4.7.0。

这样，您将使用 “SkiaSharp” 作为windows系统的依赖项。Net6项目。*请注意，使用 “SkiaSharp” 作为依赖项的版本不支持打印到打印机功能。*
## 运行的 Aspose.3D。Linux上的Net6

请参考 Windows 上的安装方法，您只能选择SkiaSharp作为Linux系统上的图形库依赖项。

您需要执行以下附加操作以确保在Linux下正确使用SkiaSharp:

1. 在Linux系统中运行以下命令:
```
apt-get update && apt-get install -y libfontconfig1
```
OR
```
apk update && apk add fontconfig 
```

2.将 nuget 包 “SkiaSharp.NativeAssets.Linux 2.88.6” 添加到您的.net6项目。

3.或者您可以选择将 nuget 包 “SkiaSharp.NativeAssets.Linux.NoDependencies 2.88.6” 添加到您的.net6项目，而不是上面的两个步骤。

### 适用于Ubuntu的Dockerfile示例

1. 将 nuget 包 “SkiaSharp.NativeAssets.Linux 2.88.6” 添加到您的.net6项目。

2.使用以下Dockerfile:
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

### 适用于Alpine的Dockerfile示例

1. 将 nuget 包 “SkiaSharp.NativeAssets.Linux 2.88.6” 添加到您的.net6项目。

2.使用以下Dockerfile:
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
