---
title: Cómo ejecutar Aspose.3D en Docker
type: docs
description: Ejecute Aspose.3D en un contenedor Docker para Linux, Windows Server y cualquier sistema operativo.
weight: 139
url: /es/net/how-to-run-aspose-3d-in-docker/
---
Los microservicios, junto con la contenedorización, permiten combinar fácilmente tecnologías. Docker le permite integrar fácilmente la funcionalidad Aspose.3D en su aplicación, independientemente de qué tecnología esté en su pila de desarrollo.

En caso de que esté apuntando a microservicios, o si la tecnología principal en su pila no es .NET, C++ o Java, pero necesita Aspose.3D, o si ya usa Docker en su pila, entonces puede estar interesado en utilizar Aspose.3D en un contenedor Docker.

## Requisitos previos

- Docker debe estar instalado en su sistema. Para obtener información sobre cómo instalar Docker en Windows o Mac, consulte los enlaces en la sección "Ver también".

- Además, tenga en cuenta que Visual Studio 2019, .NET Core 3,1 SDK se utiliza en el ejemplo, que se proporciona a continuación.


## Aplicación

En este ejemplo, creará una aplicación de consola sencilla que genera un archivo 3D y lo guardará en todos los formatos de guardado compatibles. La aplicación se puede construir y ejecutar en Docker.

### Creación de la aplicación de consola

Para crear el programa, siga los pasos a continuación:
1. Una vez instalado Docker, asegúrese de que utiliza Linux Containers (predeterminado). Si es necesario, seleccione la opción Cambiar a contenedores Linux en el menú de escritorios de Docker.
1. En Visual Studio, cree una aplicación de consola .NET Core.<br>
¡! [Todo: image_alt_text](create-a-new-project.png)<br>
1. Instale la última versión de Aspose.3D desde NuGet.<br>
¡! [Todo: image_alt_text](nuget-aspose-3d.png)<br>
1. Dado que la aplicación se ejecutará en Linux, se deben instalar los activos nativos de Linux apropiados. Comience con la imagen base dotnet core sdk 3,1 e instale la libc6-dev libgdiplus.
1. Después de agregar todas las dependencias requeridas, escriba un programa simple que cree un plano y cambie su orientación y guárdelo en todos los formatos de guardado compatibles:<br>
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

Tenga en cuenta que la carpeta "TestOut" se especifica como una carpeta de salida para guardar documentos de salida. Al ejecutar la aplicación en Docker, se montará una carpeta en la máquina host en esta carpeta en el contenedor. Esto le permitirá ver fácilmente la salida generada por Aspose.3D en el contenedor Docker.

### Configuración de un Dockerfile

El siguiente paso es crear y configurar el Dockerfile.

1. Cree el Dockerfile y píntelo junto al archivo de solución de su aplicación. Mantenga este nombre de archivo sin extensión (predeterminado).
1. En Dockerfile, especifique:

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

Lo anterior es un Dockerfile simple, que contiene las siguientes instrucciones:

- Imagen del SDK que se va a utilizar. Aquí está el. Imagen de Net Core SDK 3,1. Docker lo descargará cuando se ejecute la compilación. La versión del SDK se especifica como una etiqueta.
- Comando para copiar todo en el contenedor, publicar la aplicación y especificar el punto de entrada.
- El comando para instalar libgdiplus se ejecuta en el contenedor. System.Drawing.Common lo requiere.

### Construir y ejecutar la aplicación en Docker

Ahora la aplicación se puede construir y ejecutar en Docker. Abra su símbolo del sistema favorito, cambie el directorio a la carpeta con la aplicación (carpeta donde se colocan el archivo de solución y el Dockerfile) y ejecute el siguiente comando:

{{< highlight "plain" >}}
docker build -t actest .
{{< /highlight >}}

La primera vez que se ejecuta este comando puede tardar más tiempo, ya que Docker necesita descargar las imágenes requeridas. Una vez completado el comando anterior, ejecute el siguiente comando:

{{< highlight "plain" >}}
docker run --mount type=bind,source=C:\Temp,target=/TestOut --rm actest from Docker
{{< /highlight >}}

{{% alert color="primary" %}} 

Preste atención al argumento de montaje, porque, como se mencionó anteriormente, una carpeta en la máquina host se monta en la carpeta del contenedor, para ver fácilmente los resultados de la ejecución de la aplicación. Las rutas en Linux son sensibles a mayúsculas y minúsculas.

{{% /alert %}}

## Imágenes que aducen Aspose.3D

- Aspose.3D for .NET El estándar no admite EMF y TIFF en Linux.


## Más ejemplos

***1. Para ejecutar la aplicación en Windows Server 2019***

- Archivo Dockerfile

{{< highlight "plain" >}}
FROM microsoft/dotnet-framework:4.7.2-sdk-windowsservercore-ltsc2019
WORKDIR /app
COPY . ./
RUN dotnet publish "Aspose.3D.Docker.csproj" -c Release -o /app/publish
ENTRYPOINT ["dotnet", "publish/Aspose.3D.Docker.dll"]
{{< /highlight >}}

- Crear imagen de Docker

{{< highlight "plain" >}}
docker build -t actest .
{{< /highlight >}}

- Ejecutar imagen de Docker

{{< highlight "plain" >}}
docker run --mount type=bind,source=C:\Temp,target=c:\TestOut --rm actest from Docker
{{< /highlight >}}

## Ver también

- [Instalar Docker Desktop en Windows](https://docs.docker.com/docker-for-windows/install/)
- [Instalar Docker Desktop en Mac](https://docs.docker.com/docker-for-mac/install/)
- [Visual Studio 2019, .NET Core 3,1 SDK](https://docs.microsoft.com/en-us/dotnet/core/install/windows?tabs=netcore31#dependencies)
- Opción [Cambiar a contenedores Linux](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers)
- Información adicional sobre [.NET SDK básico](https://hub.docker.com/_/microsoft-dotnet-sdk)
