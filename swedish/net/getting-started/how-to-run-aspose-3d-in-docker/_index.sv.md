---
title: Hur man kör Aspose.3D i dockar
type: docs
description: Kör Aspose.3D i en Dockerbehållare för Linux, Windows-server och något operativsystem.
weight: 139
url: /sv/net/how-to-run-aspose-3d-in-docker/
---
Mikrotjänster tillsammans med containerisering gör det möjligt att enkelt kombinera teknik. Dockaren låter dig enkelt integrera Aspose. 3D funktionalitet i din applikation, oavsett vilken teknik som finns i din utvecklingsstack.

Om du riktar på mikrotjänster, eller om huvudteknologin i din stack inte är .NET, C++ eller Java, men du behöver Aspose. 3D funktionalitet, eller om du redan använder Docker i din stack, då kan du vara intresserad av att använda Aspose. 3D i en Dockerbehållare.

## Förutsättningar

- Dockaren måste vara installerad på ditt system. För information om hur du installerar Docker på Windows eller Mac, se länkarna i avsnittet "Se också".

- Observera också att Visual Studio 2019, .NET Core 3.1 SDK används i exemplet nedan.


## Tillämpning

I det här exemplet skapar du ett enkelt konsolprogram som skapar en 3D-fil och sparar den i alla format som stöds. Programmet kan sedan byggas och köras i Docker.

### Skapa konsolprogrammet

För att skapa programmet, följ nedanstående steg:
1. När Docker är installerat, se till att det använder Linux Containers (standard). Om det behövs, välj alternativet Växla till Linux-behållare i Docker-skrivbordsmenyn.
1. I Visual Studio, skapa en applikation med .NET Core-konsol.<br>
![todo:image_alt_text](create-a-new-project.png)<br>
1. Installera den senaste versionen Aspose.3D från NuGet.<br>
![todo:image_alt_text](nuget-aspose-3d.png)<br>
1. Eftersom ansökan kommer att köras på Linux måste lämpliga inhemska Linuxtillgångar installeras. Börja med dotnet core sdk 3.1 basebild och installera libgdiplus libc6-dev.
1. Efter att lägga till alla nödvändiga beroenden, skriv ett enkelt program som skapar ett plan och ändrar dess orientering och sparar det till alla stödda sparformat:<br>
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

Observera att mappen "TestOut" anges som en utdatamapp för att spara utdatadokument. När programmet körs i Docker, monteras en mapp på värdmaskinen till den här mappen i behållaren. Det här gör att du enkelt kan visa utmatningen som genererats av Aspose.3D i Dockbehållaren.

### Anpassa en Dockerfil

Nästa steg är att skapa och konfigurera Dockerfilen.

1. Skapa Dockerfilen och placera den bredvid lösningsfilen i din ansökan. Behåll filnamnet utan filändelse (standard).
1. Ange i Dockerfilen:

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

Ovanstående är en enkel Dockerfile, som innehåller följande instruktioner:

- SDK-bilden som ska användas. Här är det. Nettkärna SDK 3.1 bild. Docker kommer att ladda ner det när byggandet körs. Versionen av SDK anges som en tagg.
- Kommandot för att kopiera allt till container, publicera programmet och ange ingångspunkten.
- Kommandot för att installera libgdiplus körs i behållaren. Detta krävs av System.Drawing.Common.

### Bygga och köra applikationen i Dockern

Nu kan programmet byggas och köras i Docker. Öppna din favoritkommando, byt katalog till mappen med programmet (mapp där lösningsfilen och Dockerfilen placeras) och kör följande kommando:

{{< highlight "plain" >}}
docker build -t actest .
{{< /highlight >}}

Första gången detta kommando körs kan det ta längre tid, eftersom Docker behöver ladda ner de nödvändiga bilderna. När föregående kommando är färdigt, kör följande kommando:

{{< highlight "plain" >}}
docker run --mount type=bind,source=C:\Temp,target=/TestOut --rm actest from Docker
{{< /highlight >}}

{{% alert color="primary" %}} 

Var uppmärksam på monteringen, eftersom, som nämnts tidigare, en mapp på värdmaskinen är monterad i containerns mapp, för att enkelt se resultaten av programmets utförande. Sökvägar i Linux är känsliga.

{{% /alert %}}

## Bilder som stöder Aspose.3D

- Aspose.3D for .NET Standard inte stöder EMF och TIFF på Linux.


## Fler exempel

***1. Att köra programmet i Windows Server 2019.***

- Dockfil

{{< highlight "plain" >}}
FROM microsoft/dotnet-framework:4.7.2-sdk-windowsservercore-ltsc2019
WORKDIR /app
COPY . ./
RUN dotnet publish "Aspose.3D.Docker.csproj" -c Release -o /app/publish
ENTRYPOINT ["dotnet", "publish/Aspose.3D.Docker.dll"]
{{< /highlight >}}

- Bygg doseringsavbildning

{{< highlight "plain" >}}
docker build -t actest .
{{< /highlight >}}

- Kör doseringsavbildning

{{< highlight "plain" >}}
docker run --mount type=bind,source=C:\Temp,target=c:\TestOut --rm actest from Docker
{{< /highlight >}}

## Se också

- [Install Docker Desktop on Windows](https://docs.docker.com/docker-for-windows/install/)
- [Install Docker Desktop on Mac](https://docs.docker.com/docker-for-mac/install/)
- [Visual Studio 2019, .NET Core 3.1 SDK](https://docs.microsoft.com/en-us/dotnet/core/install/windows?tabs=netcore31#dependencies)
- [Byt till Linux-behållare](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers) väljare
- Ytterligare information på [.NET Core SDK](https://hub.docker.com/_/microsoft-dotnet-sdk).
