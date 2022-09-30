---
title: Cómo ejecutar los ejemplos
type: docs
weight: 70
url: /es/net/how-to-run-the-examples/
description: Aquí le guiaremos cómo ejecutar los ejemplos de Aspose.3D for .NET.
---
## **Requisitos del software**
Asegúrese de cumplir con los siguientes requisitos antes de descargar y ejecutar los ejemplos.

1. Visual Studio 2010 o superior
1. NuGet Package Manager instalado en Visual Studio. Asegúrese de que la última versión NuGet API esté instalada en Visual Studio. Para obtener más información sobre cómo instalar el administrador de paquetes NuGet, consulte<https://docs.microsoft.com/en-us/nuget/install-nuget-client-tools>
1. Vaya a Herramientas-> Opciones->NuGet Administrador de paquetes-> Fuentes de paquetes y asegúrese de que la opción**nuget org**Se comprueba
1. El proyecto de ejemplo utiliza la función de restauración automática de paquetes NuGet, por lo tanto, debe tener una conexión a Internet activa. Si no tiene una conexión a Internet activa en la máquina donde se deben ejecutar ejemplos, consulte[Instalación](/3d/es/net/installation/)Y agregue manualmente la referencia a Aspose.3D.dll en el proyecto de ejemplo.
## **Descargar desde GitHub**
Todos los ejemplos de Aspose.3D for .NET están alojados en[GitHub](https://github.com/aspose-3d/Aspose.3D-for-.NET).

- Puede clonar el repositorio utilizando su cliente GitHub favorito o descargar el archivo ZIP desde[Aquí](https://github.com/aspose-3d/Aspose.3D-for-.NET/archive/master.zip).
- Extraiga el contenido del archivo ZIP a cualquier carpeta de su ordenador. Todos los ejemplos se encuentran en la carpeta `Examples`.
- Hay un archivo de solución en el proyecto que contiene ejemplos C#.
- Los proyectos se crean en Visual Studio 2013, pero los archivos de solución son compatibles con Visual Studio 2010 SP1 y superiores.
- Abra el archivo de solución en Visual Studio y construya el proyecto.
- En la primera ejecución, las dependencias se descargarán automáticamente a través de NuGet.
- `Data` carpeta en la carpeta raíz de `Examples` contiene archivos de entrada que CSharp ejemplos utilizados. Es obligatorio descargar la carpeta `Data` junto con el proyecto de ejemplos.
- Abra el archivo `RunExamples.cs`, todos los ejemplos se llaman desde aquí.
- Anule el comentario de los ejemplos desde el proyecto.

No dude en comunicarse con nuestros Foros si tiene algún problema para configurar o ejecutar los ejemplos.
## **Contribuir**
Si te gusta añadir o mejorar un ejemplo, te animamos a contribuir al proyecto. Todos los ejemplos y proyectos de exhibición en este repositorio son de código abierto y se pueden utilizar libremente en sus propias aplicaciones.

Para contribuir, puede bifurcar el repositorio, editar el código fuente y crear una solicitud de extracción. Revisaremos los cambios y los incluiremos en el repositorio si resulta útil.
