---
title: Cómo ejecutar Aspose.3D para. Por Net6
type: docs
description: Cómo ejecutar Aspose.3D para. Por Net6
weight: 138
url: /es/net/how-to-run-aspose-3d-for-net6/
---
## Descripción general

Para el. Las plataformas NET6 (o posteriores), en comparación con las plataformas anteriores (.netcore31 o anteriores), una diferencia importante es sobre la biblioteca de gráficos.
En este oficial [Documento Microsoft](https://learn.microsoft.com/en-gb/dotnet/core/compatibility/core-libraries/6.0/system-drawing-common-windows-only), explica. NET6 o versiones posteriores de la biblioteca de gráficos "System.Drawing.Common" sólo se admitirá en Windows, y da recomendaciones para reemplazar la biblioteca de gráficos.

Para el producto Apose.3D, hemos llevado a cabo la evaluación y hemos completado la migración de la biblioteca de gráficos. Usamos SkiaSharp en lugar de System.Drawing.Common en sistemas que no son Windows, como se sugiere en la documentación oficial de Microsoft. Tenga en cuenta que este cambio crítico tendrá efecto en Aspose.3D 22.10.1 o posterior para. Net6.

Para. netcore31 o antes, por compatibilidad y estabilidad, actualmente todavía usamos la biblioteca de gráficos "System.Drawing.Common". Las dependencias de. netcore31 o anteriores son las siguientes:
- System.Drawing.Common, 4.7.0.
- System.Security.Cryptography.Pkcs, 5.0.1.
- System.Text.Encoding.CodePages, 4.7.0.

## Ejecute Aspose.3D para. Net6 en Windows

Primero puede crear una aplicación. net6 con VS2022, luego puede elegir las siguientes opciones de instalación:

### Instalar a través de nuget

1. Busca Aspose.3D desde NuGet: [Aspose.3D for .NET NuGet Paquete](https://www.nuget.org/packages/Aspose.3D/).
También puede instalar Aspose.3D desde el administrador de paquetes Nuget en VS2022.

2. "SkiaSharp" o "System.Drawing.Common" se instalarán automáticamente como una dependencia de Aspose.3D 22.10.1 o posterior para. Plataformas Net6, que depende de la configuración de "Target OS" en su proyecto.
- Establezca el "Target OS" en "Windows" para su proyecto, usará "System.Drawing.Common" como una dependencia en su sistema de Windows para. Proyecto Net6. En esta configuración, el resultado del dibujo está más cerca de. netcore31 o antes.
**¡! [Config objetivo OS] (TargetOS.png)**
- Establezca el "Target OS" en "None" u otras opciones para su proyecto, usará "SkiaSharp" como una dependencia en su sistema de Windows para. Proyecto Net6.*Tenga en cuenta que la versión que utiliza "SkiaSharp" como dependencia no admite la función de impresión a impresora.*

### Instalar a través de msi o DLL

1. [Descargar Aspose.3D.msi o DLL](https://releases.aspose.com/3d/net/)

2. Abra el directorio de instalación o el directorio DLL y, a continuación, seleccione el paso 3 o 4 a continuación:

3. localice el subdirectorio "net6.0-windows", agregue el Aspose.3D.dll a su aplicación. net6. Agregue manualmente los siguientes paquetes nuget a su proyecto. net6:
- System.Drawing.Common, 4.7.0.
- System.Security.Cryptography.Pkcs, 6.0.3.
- System.Text.Encoding.CodePages, 4.7.0.

De esta manera, usará "System.Drawing.Common" como una dependencia en su sistema de Windows para. Proyecto Net6. En esta configuración, el resultado del dibujo está más cerca de. netcore31 o antes.

4. localice el subdirectorio "net6.0", agregue el Aspose.3D.dll a su aplicación. net6. Agregue manualmente los siguientes paquetes nuget a su proyecto. net6:
- SkiaSharp, 2.88.6.
- System.Security.Cryptography.Pkcs, 6.0.3.
- System.Text.Encoding.CodePages, 4.7.0.

De esta manera, usará "SkiaSharp" como una dependencia en su sistema de Windows para. Proyecto Net6.*Tenga en cuenta que la versión que utiliza "SkiaSharp" como dependencia no admite la función de impresión a impresora.*
## Ejecute Aspose.3D para. Net6 en Linux

Consulte el método de instalación en Windows, solo puede seleccionar SkiaSharp como una dependencia de la biblioteca de gráficos en el sistema Linux.

Debe realizar las siguientes operaciones adicionales para garantizar el uso adecuado de SkiaSharp en Linux:

1. Ejecute el siguiente comando en su sistema Linux:
```
apt-get update && apt-get install -y libfontconfig1
```
OR
```
apk update && apk add fontconfig 
```

2. Agregue los paquetes nuget "SkiaSharp.NativeAssets.Linux 2. 88,6" a su proyecto. net6.

3. O puede optar por agregar paquetes nuget "SkiaSharp.NativeAssets.Linux.NoDependencies 2. 88,6" a su proyecto. net6, en lugar de los dos pasos anteriores.

### Ejemplo de Dockerfile para Ubuntu

1. Agregue los paquetes nuget "SkiaSharp.NativeAssets.Linux 2. 88,6" a su proyecto. net6.

2. Utilice el siguiente Dockerfile:
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

### Ejemplo de Dockerfile para Alpine

1. Agregue los paquetes nuget "SkiaSharp.NativeAssets.Linux 2. 88,6" a su proyecto. net6.

2. Utilice el siguiente Dockerfile:
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
