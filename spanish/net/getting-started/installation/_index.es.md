---
title: Installation
type: docs
weight: 40
url: /es/net/installation/
description: Este artículo explica cómo instalar Aspose.3D fo r.NET - C# 3D Manipulación y conversión de formatos de archivo API utilizando NuGet y Package Manager Console.
---
Este artículo explica cómo instalar Aspose.3D fo r.NET - C# 3D Manipulación y conversión de formatos de archivo API utilizando NuGet y Package Manager Console.

##  **Instalación de Aspose.3D for .NET a través de NuGet**
NuGet es un sistema gratuito de gestión de paquetes centrado en el desarrollador de código abierto para la plataforma .NET con la intención de simplificar el proceso de incorporación de bibliotecas de terceros en una aplicación .NET durante el desarrollo. Es una extensión de Visual Studio que facilita agregar, quitar y actualizar bibliotecas y herramientas en proyectos de Visual Studio que usan .NET Framework. Una biblioteca o herramienta se puede compartir fácilmente con otros desarrolladores creando un paquete NuGet y almacenándolo dentro de un repositorio NuGet. Al instalar el paquete, NuGet copia los archivos en la solución y realiza automáticamente los cambios necesarios, como agregar referencias y cambiar los archivos app.config o web.config. Si decide quitar la biblioteca, NuGet quita los archivos e invierte los cambios realizados en el proyecto para que no quede ningún desorden.
###  **Haciendo referencia a Aspose.3D for .NET**
Aprovechando esta maravillosa característica, hemos agrupado las bibliotecas [Aspose.3D for .NET](https://www.nuget.org/packages/Aspose.3D) en un paquete NuGet y lo hemos subido a un repositorio NuGet. Con esta opción, se beneficia de usar Aspose.3D for .NET sin instalar este componente en su sistema. NuGet se ejecuta en Visual Studio 2010 y versiones superiores, Visual Web Developer 2010 y Windows Phone Developer Tools 7,1. En nuestras pruebas, lo hemos probado con Visual Studio 2015 Ultimate.

Para empezar:

1. Abra su solución o proyecto en Visual Studio.
1. Agregue NuGet Package Manager como una extensión de Visual Studio:
1. Seleccione el**Herramientas**Menú seguido por**Extension Manager**.
1. Seleccione**Galería en línea**Para obtener una lista completa de los paquetes disponibles en línea.
1. Seleccione**NuGet Administrador de paquetes**.
1. Haga clic en**Descargar**.
1. Una vez instalado el Administrador de paquetes, reinicie Visual Studio para que los cambios entren en vigor.
Cuando se instala el Administrador de paquetes NuGet, puede buscar, instalar, eliminar y actualizar paquetes desde el**Administrar paquetes NuGet**Ventana, o mediante el uso de comandos de la línea de comandos de PowerShell en el**Package Manager Console**Ventana dedicada de Visual Studio. Puede encontrar ambas opciones si selecciona el**Herramientas**Seguido por el**Administrador de paquetes de biblioteca**.
###  **Instalar-Empaquetar usando la consola de Package Manager**
Para hacer referencia al componente mediante la consola del administrador de paquetes:

1. Abra la aplicación .NET en Visual Studio.
1. En el**Herramientas**Menú, seleccione**Administrador de paquetes de biblioteca**Y luego**Package Manager Console**.
1. Escriba el comando "Install-Package Aspose.3D" para instalar la última versión completa, o escriba el comando "Install-Package Aspose.3D -prerrelease" para instalar la última versión, incluidas las correcciones en caliente.
1. Prensa**Entrar**.
###  **Actualizar paquete con la consola de Package Manager**
Si ya ha hecho referencia al componente a través de NuGet, siga estos pasos para actualizar la referencia a la última versión:

1. Abra la aplicación .NET en Visual Studio.
1. Desde el**Herramientas**Menú, seleccione**Administrador de paquetes de biblioteca**, Seguido por el**Package Manager Console**Para abrir la consola de Package Manager.
1. Escriba el comando “Update-Package Aspose.3D” para hacer referencia a la última versión completa, o escriba el comando “Update-Package Aspose.3D -prerrelease” para instalar la última versión, incluidas las correcciones en caliente.
1. Prensa**Entrar**.
###  **Instalar-Empaquetar usando la interfaz gráfica del Administrador de paquetes**
Siga estos pasos para hacer referencia al componente mediante la GUI del administrador de paquetes:

1. Abra la aplicación .NET en Visual Studio.
1. Desde el**Herramientas**Menú, seleccione**Administrador de paquetes de biblioteca**Y**Administrar paquetes NuGet**Desde el**Solución**Opción.
También puede obtener una opción similar en el Explorador de soluciones:
1. Haga clic con el botón derecho en el nombre del proyecto.
1. Seleccione**Administrar paquetes NuGet**.
1. Seleccionar**En línea**Desde el menú de la izquierda.
1. Tipo**Aspose.3D**En el cuadro de búsqueda para encontrar Aspose.3D for .NET.
1. Haga clic en**Instalar/actualizar**Junto a la última versión de Aspose.3D for .NET.
