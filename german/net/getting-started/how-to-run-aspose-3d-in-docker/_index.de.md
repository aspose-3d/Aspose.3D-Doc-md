---
title: So führen Sie Aspose.3D in Docker aus
type: docs
description: Führen Sie Aspose.3D in einem Docker-Container für Linux, Windows Server und ein beliebiges Betriebs system aus.
weight: 139
url: /de/net/how-to-run-aspose-3d-in-docker/
---
Micros ervices in Verbindung mit Container isierung ermöglichen es, Technologien leicht zu kombinieren. Mit Docker können Sie auf einfache Weise Aspose.3D-Funktional ität in Ihre Anwendung integrieren, unabhängig davon, welche Technologie sich in Ihrem Entwicklungs stapel befindet.

Falls Sie auf Mikros ervices abzielen oder wenn die Haupt technologie in Ihrem Stack nicht .NET, C++ oder Java ist, sondern Sie Aspose benötigen. 3D Funktional ität, oder wenn Sie Docker bereits in Ihrem Stack verwenden, dann könnten Sie daran interessiert sein, Aspose zu verwenden. 3D in einem Docker-Container.

## Voraussetzungen

- Docker muss auf Ihrem System installiert sein. Informationen zur Installation von Docker auf Windows oder Mac finden Sie in den Links im Abschnitt "Siehe auch".

- Beachten Sie auch, dass Visual Studio 2019, .NET Core 3.1 SDK im folgenden Beispiel verwendet wird.


## Anwendung

In diesem Beispiel erstellen Sie eine einfache Konsolen anwendung, die eine 3D-Datei generiert und in allen unterstützten Speicher formaten speichert. Die Anwendung kann dann in Docker erstellt und ausgeführt werden.

### Erstellen der Konsolen anwendung

Um das Programm zu erstellen, folgen Sie den folgenden Schritten:
1. Sobald Docker installiert ist, stellen Sie sicher, dass Linux-Container verwendet werden (Standard). Wählen Sie bei Bedarf die Option Zu Linux-Containern wechseln aus dem Menü Docker-Desktops.
1. Erstellen Sie in Visual Studio eine .NET Core-Konsolen anwendung.<br>
! [Todo: image_alt_text](create-a-new-project.png)<br>
1. Installieren Sie die neueste Version Aspose.3D von NuGet.<br>
! [Todo: image_alt_text](nuget-aspose-3d.png)<br>
1. Da die Anwendung unter Linux ausgeführt wird, müssen die entsprechenden nativen Linux-Assets installiert werden. Beginnen Sie mit dem dotnet core sdk 3.1 base image und installieren Sie libgdiplus libc6-dev.
1. Nachdem Sie alle erforderlichen Abhängigkeiten hinzugefügt haben, schreiben Sie ein einfaches Programm, das eine Ebene erstellt und ihre Ausrichtung ändert, und speichern Sie sie in allen unterstützten Speicher formaten:<br>
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

Beachten Sie, dass der Ordner „ TestOut “als Ausgabe ordner zum Speichern von Ausgabe dokumenten angegeben ist. Wenn Sie die Anwendung in Docker ausführen, wird ein Ordner auf dem Host computer an diesen Ordner im Container montiert. Auf diese Weise können Sie die von Aspose.3D erzeugte Ausgabe im Docker-Container einfach anzeigen.

### Eine Docker file konfigurieren

Der nächste Schritt besteht darin, die Docker file zu erstellen und zu konfigurieren.

1. Erstellen Sie die Docker file und platzieren Sie sie neben der Lösungs datei Ihrer Anwendung. Behalten Sie diesen Dateinamen ohne Erweiterung bei (Standard).
1. Geben Sie im Docker file Folgendes an:

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

Das Obige ist eine einfache Docker file, die die folgenden Anweisungen enthält:

- Das zu verwendende SDK-Image. Hier ist es die. Net Core SDK 3.1 Bild. Docker wird es herunter laden, wenn der Build ausgeführt wird. Die Version von SDK wird als Tag angegeben.
- Der Befehl, um alles in den Container zu kopieren, die Anwendung zu veröffentlichen und den Einstiegs punkt anzugeben.
- Der Befehl zum Installieren von libgdiplus wird im Container ausgeführt. Dies wird von System.Drawing.Common benötigt.

### Erstellen und Ausführen der Anwendung in Docker

Jetzt kann die Anwendung in Docker erstellt und ausgeführt werden. Öffnen Sie Ihre bevorzugte Eingabe aufforderung, ändern Sie das Verzeichnis in den Ordner mit der Anwendung (Ordner, in dem die Lösungs datei und die Docker datei platziert sind) und führen Sie den folgenden Befehl aus:

{{< highlight "plain" >}}
docker build -t actest .
{{< /highlight >}}

Wenn dieser Befehl zum ersten Mal ausgeführt wird, kann dies länger dauern, da Docker die erforderlichen Bilder herunter laden muss. Sobald der vorherige Befehl abgeschlossen ist, führen Sie den folgenden Befehl aus:

{{< highlight "plain" >}}
docker run --mount type=bind,source=C:\Temp,target=/TestOut --rm actest from Docker
{{< /highlight >}}

{{% alert color="primary" %}} 

Achten Sie auf das Mount-Argument, da, wie bereits erwähnt, ein Ordner auf dem Host-Computer in den Ordner des Containers eingebaut ist, um die Ergebnisse der Anwendungs ausführung leicht anzuzeigen. Wege in Linux sind fall empfindlich.

{{% /alert %}}

## Bilder mit Unterstützung von Aspose.3D

- Aspose.3D for .NET Standard unterstützt EMF und TIFF unter Linux nicht.


## Weitere Beispiele

***1. Um die Anwendung in Windows Server 2019 auszuführen***

- Docker file

{{< highlight "plain" >}}
FROM microsoft/dotnet-framework:4.7.2-sdk-windowsservercore-ltsc2019
WORKDIR /app
COPY . ./
RUN dotnet publish "Aspose.3D.Docker.csproj" -c Release -o /app/publish
ENTRYPOINT ["dotnet", "publish/Aspose.3D.Docker.dll"]
{{< /highlight >}}

- Docker-Image erstellen

{{< highlight "plain" >}}
docker build -t actest .
{{< /highlight >}}

- Docker-Image ausführen

{{< highlight "plain" >}}
docker run --mount type=bind,source=C:\Temp,target=c:\TestOut --rm actest from Docker
{{< /highlight >}}

## Siehe auch

- [Installieren Sie Docker Desktop auf Windows](https://docs.docker.com/docker-for-windows/install/)
- [Installieren Sie Docker Desktop auf dem Mac](https://docs.docker.com/docker-for-mac/install/)
- [Visual Studio 2019, .NET Core 3.1 SDK](https://docs.microsoft.com/en-us/dotnet/core/install/windows?tabs=netcore31#dependencies)
- [Zu Linux-Containern wechseln](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers) Option
- Zusätzliche Informationen über [.NET Kern-SDK](https://hub.docker.com/_/microsoft-dotnet-sdk)
