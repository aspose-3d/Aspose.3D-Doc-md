---
title: Come eseguire Aspose.3D in Docker
type: docs
description: Esegui Aspose.3D in un contenitore Docker per Linux, Windows Server e qualsiasi sistema operativo.
weight: 139
url: /it/net/how-to-run-aspose-3d-in-docker/
---
I microservizi, in combinazione con la containerizzazione, consentono di combinare facilmente le tecnologie. Docker consente di integrare facilmente Aspose.3D funzionalità nell'applicazione, indipendentemente dalla tecnologia presente nello stack di sviluppo.

Nel caso in cui ti rivolgi ai microservizi o se la tecnologia principale nello stack non è .NET, C++ o Java, ma hai bisogno di Aspose.3D funzionalità, o se usi già Docker nello stack, potresti essere interessato a utilizzare Aspose.3D in un contenitore Docker.

## Prerequisiti

- Docker deve essere installato sul tuo sistema. Per informazioni su come installare Docker su Windows o Mac, fare riferimento ai collegamenti nella sezione "Vedi anche".

- Inoltre, si noti che Visual Studio 2019, .NET Core 3.1 SDK viene utilizzato nell'esempio, fornito di seguito.


## Applicazione

In questo esempio, si creerà una semplice applicazione per console che genera un file 3D e lo si salverà in tutti i formati di salvataggio supportati. L'applicazione può quindi essere costruita ed eseguita in Docker.

### Creazione dell'applicazione Console

Per creare il programma, seguire i passaggi seguenti:
1. Una volta installato Docker, assicurati che utilizzi Linux Containers (impostazione predefinita). Se necessario, selezionare l'opzione Passa ai contenitori Linux dal menu Docker Desktops.
1. In Visual Studio, creare un'applicazione console Core .NET.<br>
! [Todo: image_alt_text](create-a-new-project.png)<br>
1. Installa l'ultima versione Aspose.3D da NuGet.<br>
! [Todo: image_alt_text](nuget-aspose-3d.png)<br>
1. Poiché l'applicazione verrà eseguita su Linux, è necessario installare le risorse Linux native appropriate. Inizia con l'immagine di base dotnet core sdk 3.1 e installa libgdiplus libc6-dev.
1. Dopo aver aggiunto tutte le dipendenze richieste, scrivere un semplice programma che crea un piano e cambia il suo orientamento e salvarlo in tutti i formati di salvataggio supportati:<br>
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

Si noti che la cartella “TestOut” è specificata come cartella di output per il salvataggio dei documenti di output. Quando si esegue l'applicazione in Docker, una cartella sulla macchina host verrà montata in questa cartella nel contenitore. Questo ti permetterà di visualizzare facilmente l'output generato da Aspose.3D nel contenitore Docker.

### Configurazione di un Dockerfile

Il prossimo passo è creare e configurare il Dockerfile.

1. Creare il Dockerfile e posizionarlo accanto al file della soluzione dell'applicazione. Conserva questo nome file senza estensione (l'impostazione predefinita).
1. Nel Dockerfile, specificare:

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

Quanto sopra è un semplice Dockerfile, che contiene le seguenti istruzioni:

- L'immagine SDK da utilizzare. Eccola la. Immagine Net Core SDK 3.1. Docker lo scaricherà quando viene eseguita la build. La versione di SDK è specificata come tag.
- Comando per copiare tutto nel contenitore, pubblicare l'applicazione e specificare il punto di ingresso.
- Il comando per installare libgdiplus viene eseguito nel contenitore. Questo è richiesto da System.Drawing.Common.

### Costruire ed eseguire l'applicazione in Docker

Ora l'applicazione può essere costruita ed eseguita in Docker. Apri il prompt dei comandi preferito, modifica la directory nella cartella con l'applicazione (cartella in cui sono posizionati il file di soluzione e il Dockerfile) ed esegui il seguente comando:

{{< highlight "plain" >}}
docker build -t actest .
{{< /highlight >}}

La prima volta che questo comando viene eseguito potrebbe richiedere più tempo, poiché Docker deve scaricare le immagini richieste. Una volta completato il comando precedente, eseguire il seguente comando:

{{< highlight "plain" >}}
docker run --mount type=bind,source=C:\Temp,target=/TestOut --rm actest from Docker
{{< /highlight >}}

{{% alert color="primary" %}} 

Prestare attenzione all'argomento mount, perché, come accennato in precedenza, una cartella sulla macchina host è montata nella cartella del contenitore, per vedere facilmente i risultati dell'esecuzione dell'applicazione. I percorsi in Linux sono sensibili al caso.

{{% /alert %}}

## Immagini che supportano Aspose.3D

- Aspose.3D for .NET Standard non supporta EMF e TIFF su Linux.


## Altri esempi

***1. Per eseguire l'applicazione in Windows Server 2019***

- Dockerfile

{{< highlight "plain" >}}
FROM microsoft/dotnet-framework:4.7.2-sdk-windowsservercore-ltsc2019
WORKDIR /app
COPY . ./
RUN dotnet publish "Aspose.3D.Docker.csproj" -c Release -o /app/publish
ENTRYPOINT ["dotnet", "publish/Aspose.3D.Docker.dll"]
{{< /highlight >}}

- Costruisci immagine Docker

{{< highlight "plain" >}}
docker build -t actest .
{{< /highlight >}}

- Esegui immagine Docker

{{< highlight "plain" >}}
docker run --mount type=bind,source=C:\Temp,target=c:\TestOut --rm actest from Docker
{{< /highlight >}}

## Vedi anche

- [Installa Docker Desktop su Windows](https://docs.docker.com/docker-for-windows/install/)
- [Installare Docker Desktop sul Mac](https://docs.docker.com/docker-for-mac/install/)
- [Visual Studio 2019, .NET Core 3.1 SDK](https://docs.microsoft.com/en-us/dotnet/core/install/windows?tabs=netcore31#dependencies)
- [Passa ai contenitori Linux](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers) opzione
- Informazioni aggiuntive su [.NET Core SDK](https://hub.docker.com/_/microsoft-dotnet-sdk)
