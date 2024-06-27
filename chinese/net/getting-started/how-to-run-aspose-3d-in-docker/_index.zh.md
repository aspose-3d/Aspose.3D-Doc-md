---
title: 如何在Docker中运行 Aspose.3D
type: docs
description: 在适用于Linux、 Windows 服务器和任何操作系统的Docker容器中运行 Aspose.3D。
weight: 139
url: /zh/net/how-to-run-aspose-3d-in-docker/
---
微服务与容器化相结合，可以轻松地组合技术。Docker允许您轻松地将 Aspose.3D 功能集成到您的应用程序中，而不管您的开发堆栈中有什么技术。

如果您的目标是微服务，或者您的堆栈中的主要技术不是 .NET 、 C++ 或 Java，但您需要 Aspose.3D 功能，或者您已经在堆栈中使用了Docker，然后，您可能有兴趣在Docker容器中使用 Aspose.3D。

## 先决条件

- Docker必须安装在您的系统上。有关如何在 Windows 或Mac上安装Docker的信息，请参阅 “另请参阅” 部分中的链接。

- 另外，请注意，下面提供的示例中使用了Visual Studio 2019，.NET 核心3.1 SDK。


## 应用

在此示例中，您将创建一个简单的控制台应用程序，该应用程序将生成一个 3D 文件并将其保存为所有支持的保存格式。然后可以在Docker中建立和运行应用程序。

### 创建控制台应用程序

要创建程序，请执行以下步骤:
1. 安装Docker后，请确保它使用Linux容器 (默认)。如有必要，从Docker桌面菜单中选择切换到Linux容器选项。
1. 在Visual Studio中，创建 .NET 核心控制台应用程序。<br>
![todo: 图像 _ alt_text](create-a-new-project.png)<br>
1. 从 NuGet 安装最新的 Aspose.3D 版本。<br>
![todo: 图像 _ alt_text](nuget-aspose-3d.png)<br>
1. 由于应用程序将在Linux上运行，因此必须安装相应的本机Linux资产。从dotnet core sdk 3.1基础映像开始，libc6-dev安装libgdiplus。
1. 添加所有必需的依赖关系后，编写一个简单的程序，创建一个平面并更改其方向，并将其保存为所有支持的保存格式:<br>
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

注意，“TestOut” 文件夹被指定为用于保存输出文档的输出文件夹。在Docker中运行应用程序时，主机上的文件夹将被挂载到容器中的此文件夹。这将使您能够轻松查看Docker容器中 Aspose.3D 生成的输出。

### 配置Dockerfile

下一步是创建和配置Dockerfile。

1. 创建Dockerfile并将其放在应用程序的解决方案文件旁边。保留此文件名，不带扩展名 (默认)。
1. 在Dockerfile中，指定:

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

以上是一个简单的Dockerfile，其中包含以下说明:

- 要使用的SDK镜像。这是。Net Core SDK 3.1映像。Docker将在构建运行时下载它。SDK的版本指定为标签。
- 将所有内容复制到容器、发布应用程序并指定入口点的命令。
- 安装libgdiplus的命令在容器中运行。这是System.Drawing.Common所要求的。

### 在Docker中构建和运行应用程序

现在可以在Docker中建立和运行应用程序。打开您喜欢的命令提示符，将目录更改为包含应用程序的文件夹 (放置解决方案文件和Dockerfile的文件夹)，然后运行以下命令:

{{< highlight "plain" >}}
docker build -t actest .
{{< /highlight >}}

第一次执行此命令可能需要更长时间，因为Docker需要下载所需的映像。完成前面的命令后，运行以下命令:

{{< highlight "plain" >}}
docker run --mount type=bind,source=C:\Temp,target=/TestOut --rm actest from Docker
{{< /highlight >}}

{{% alert color="primary" %}} 

请注意mount参数，因为如前所述，主机上的文件夹被挂载到容器的文件夹中，以便轻松查看应用程序执行的结果。Linux中的路径区分大小写。

{{% /alert %}}

## 支持 Aspose.3D 的图像

- Aspose.3D for .NET 标准在Linux上不支持EMF和TIFF。


## 更多示例

***1.在 Windows 服务器2019中运行应用程序***

- Dockerfile

{{< highlight "plain" >}}
FROM microsoft/dotnet-framework:4.7.2-sdk-windowsservercore-ltsc2019
WORKDIR /app
COPY . ./
RUN dotnet publish "Aspose.3D.Docker.csproj" -c Release -o /app/publish
ENTRYPOINT ["dotnet", "publish/Aspose.3D.Docker.dll"]
{{< /highlight >}}

- 构建Docker映像

{{< highlight "plain" >}}
docker build -t actest .
{{< /highlight >}}

- 运行Docker映像

{{< highlight "plain" >}}
docker run --mount type=bind,source=C:\Temp,target=c:\TestOut --rm actest from Docker
{{< /highlight >}}

## 另见

- [在 Windows 上安装Docker Desktop](https://docs.docker.com/docker-for-windows/install/)
- [在Mac上安装Docker桌面](https://docs.docker.com/docker-for-mac/install/)
- [Visual Studio 2019，.NET 核心3.1 SDK](https://docs.microsoft.com/en-us/dotnet/core/install/windows?tabs=netcore31#dependencies)
- [切换到Linux容器](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers) 选项
- 关于 [.NET 核心SDK](https://hub.docker.com/_/microsoft-dotnet-sdk) 的其他信息
