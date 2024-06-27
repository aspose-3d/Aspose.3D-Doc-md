---
title: Comment exécuter Aspose.3D dans Docker
type: docs
description: Exécutez Aspose.3D dans un conteneur Docker pour Linux, Windows Server et n'importe quel système d'exploitation.
weight: 139
url: /fr/net/how-to-run-aspose-3d-in-docker/
---
Les microservices, associés à la conteneurisation, permettent de combiner facilement les technologies. Docker vous permet d'intégrer facilement la fonctionnalité Aspose.3D dans votre application, quelle que soit la technologie de votre pile de développement.

Dans le cas où vous ciblez des microservices, ou si la technologie principale de votre pile n'est pas .NET, C++ ou Java, mais vous avez besoin de Aspose.3D, ou si vous utilisez déjà Docker dans votre pile, vous pouvez être intéressé par l'utilisation de Aspose.3D dans un conteneur Docker.

## Prérequis

- Docker doit être installé sur votre système. Pour plus d'informations sur la façon d'installer Docker sur Windows ou Mac, reportez-vous aux liens dans la section "Voir aussi".

- Notez également que le SDK Visual Studio 2019, .NET Core 3.1 est utilisé dans l'exemple, fourni ci-dessous.


## Application

Dans cet exemple, vous allez créer une application de console simple qui génère un fichier 3D et l'enregistrer dans tous les formats de sauvegarde pris en charge. L'application peut ensuite être construite et exécutée dans Docker.

### Créer l'application console

Pour créer le programme, suivez les étapes ci-dessous:
1. Une fois Docker installé, assurez-vous qu'il utilise des conteneurs Linux (par défaut). Si nécessaire, sélectionnez l'option Passer aux conteneurs Linux dans le menu Docker Desktops.
1. Dans Visual Studio, créez une application console .NET Core.<br>
! [Tout le monde: image_alt_text](create-a-new-project.png)<br>
1. Installez la dernière version de Aspose.3D à partir de NuGet.<br>
! [Tout le monde: image_alt_text](nuget-aspose-3d.png)<br>
1. Puisque l'application sera exécutée sur Linux, les ressources Linux natives appropriées doivent être installées. Commencez avec l'image de base dotnet core sdk 3.1 et installez libc6-dev libgdiplus.
1. Après avoir ajouté toutes les dépendances requises, écrivez un programme simple qui crée un plan et modifie son orientation et enregistrez-le dans tous les formats de sauvegarde pris en charge:<br>
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

Notez que le dossier «TestOut» est spécifié comme dossier de sortie pour la sauvegarde des documents de sortie. Lors de l'exécution de l'application dans Docker, un dossier sur la machine hôte sera monté sur ce dossier dans le conteneur. Cela vous permettra de visualiser facilement la sortie générée par Aspose.3D dans le conteneur Docker.

### Configuration d'un fichier Dockerfile

L'étape suivante consiste à créer et configurer le fichier Dockerfile.

1. Créez le fichier Dockerfile et placez-le à côté du fichier de solution de votre application. Conservez ce nom de fichier sans extension (valeur par défaut).
1. Dans le Dockerfile, spécifiez:

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

Ce qui précède est un simple fichier Dockerfile, qui contient les instructions suivantes:

- L'image SDK à utiliser. Ici c'est le. Net Core SDK 3.1 image. Docker le téléchargera lorsque la compilation sera exécutée. La version du SDK est spécifiée sous forme de balise.
- La commande pour tout copier dans le conteneur, publier l'application et spécifier le point d'entrée.
- La commande pour installer libgdiplus est exécutée dans le conteneur. Ceci est requis par System.Drawing.Common.

### Création et exécution de l'application dans Docker

Maintenant, l'application peut être construite et exécutée dans Docker. Ouvrez votre invite de commande préférée, changez de répertoire dans le dossier contenant l'application (dossier dans lequel le fichier solution et le fichier Dockerfile sont placés) et exécutez la commande suivante:

{{< highlight "plain" >}}
docker build -t actest .
{{< /highlight >}}

La première fois que cette commande est exécutée, cela peut prendre plus de temps, car Docker doit télécharger les images requises. Une fois la commande précédente terminée, exécutez la commande suivante:

{{< highlight "plain" >}}
docker run --mount type=bind,source=C:\Temp,target=/TestOut --rm actest from Docker
{{< /highlight >}}

{{% alert color="primary" %}} 

Faites attention à l'argument mount, car, comme mentionné précédemment, un dossier sur la machine hôte est monté dans le dossier du conteneur, pour voir facilement les résultats de l'exécution de l'application. Les chemins sous Linux sont sensibles à la casse.

{{% /alert %}}

## Images à l'appui de Aspose.3D

- Aspose.3D for .NET Standard ne supporte pas EMF et TIFF sous Linux.


## Plus d'exemples

***1. Pour exécuter l'application dans Windows Server 2019***

- Dockerfile

{{< highlight "plain" >}}
FROM microsoft/dotnet-framework:4.7.2-sdk-windowsservercore-ltsc2019
WORKDIR /app
COPY . ./
RUN dotnet publish "Aspose.3D.Docker.csproj" -c Release -o /app/publish
ENTRYPOINT ["dotnet", "publish/Aspose.3D.Docker.dll"]
{{< /highlight >}}

- Construire une image Docker

{{< highlight "plain" >}}
docker build -t actest .
{{< /highlight >}}

- Exécuter Docker Image

{{< highlight "plain" >}}
docker run --mount type=bind,source=C:\Temp,target=c:\TestOut --rm actest from Docker
{{< /highlight >}}

## Voir aussi

- [Installer Docker Desktop sur Windows](https://docs.docker.com/docker-for-windows/install/)
- [Installer Docker Desktop sur Mac](https://docs.docker.com/docker-for-mac/install/)
- [Visual Studio 2019, .NET Core 3.1 SDK](https://docs.microsoft.com/en-us/dotnet/core/install/windows?tabs=netcore31#dependencies)
- [Passer aux conteneurs Linux](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers) option
- Informations complémentaires sur [.NET Core SDK](https://hub.docker.com/_/microsoft-dotnet-sdk)
