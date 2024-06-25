---
title: Hur man kör Aspose.3D för . Nett6
type: docs
description: Hur man kör Aspose.3D för . Nett6
weight: 138
url: /sv/net/how-to-run-aspose-3d-for-net6/
---
## Översikt

För . NET6 (eller senare) plattformar, jämfört med tidigare plattformar (. Netcore31 eller tidigare), en viktig skillnad handlar om grafikbiblioteket.
I denna officiella [Microsoft DokumentName](https://learn.microsoft.com/en-gb/dotnet/core/compatibility/core-libraries/6.0/system-drawing-common-windows-only), förklarar det för . NET6 eller senare släpper grafikbiblioteket "System. Ritar. Gemensam" stöds endast på Windows, och ger rekommendationer för att ersätta grafikbiblioteket.

För Apose.3D produkt har vi genomfört utvärderingen och har slutfört migreringen av grafikbiblioteket. Vi använder SkiaSharp istället för System. Ritar. Vanligt i icke- Windows system, som föreslås i Microsoft officiella dokumentation. Observera att denna kritiska ändring träder i kraft i Aspose.3D 22.10.1 eller senare för . Net6.

För . Netcore31 eller tidigare, för kompatibilitet och stabilitet, för närvarande använder vi fortfarande "System. Ritar. Gemensamt grafikbibliotek. Beroenden för .netcore31 eller tidigare är följande:
- System.Ritning. Vanlig, 4.7.0.
- System.Security.Cryptography.Pkcs, 5.0.1.
- System.Text.kodning.CodeSider, 4.7.0.

## Kör Aspose.3D för . Nät 6 på Windows

Först kan du skapa en .net6-applikation med VS2022, sedan kan du välja följande installationsalternativ:

### Installera via nuget @ info: whatsthis

1. Sök efter Aspose.3D från NuGet: [Aspose.3D for .NET NuGet Paket](https://www.nuget.org/packages/Aspose.3D/).
Du kan också installera Aspose.3D från pakethanteraren Nuget i VS2022.

2. "SkiaSharp" eller "System. Ritar. Common" kommer att installeras automatiskt som ett beroende på Aspose. 3D 22.10. 1 eller senare för . Net6-plattformar, som beror på "Target OS"-konfigurationen i ditt projekt.
- Ange "Målet OS" till "Windows" för ditt projekt, du kommer att använda "System. Ritar. Vanligt "som ett beroende av ditt Windows system för . Net6-projekt. I denna konfiguration är resultatet av ritningen närmare .netcore31 eller tidigare.
**! [Config-mål OS](TargetOS.png)**
- Ställ in " Målet OS" till "Ingen" eller andra alternativ för ditt projekt, du kommer att använda "SkiaSharp" som ett beroende av ditt Windows system för . Net6-projekt.*Observera att den version som använder "SkiaSharp" som beroende stöder inte utskrift till skrivarfunktionen.*

### Installera via msi eller DLL

1. [Download Aspose.3D.msi or DLL](https://releases.aspose.com/3d/net/)

2. Öppna installationskatalogen eller DLL-katalogen, välj sedan steg 3 eller 4 nedan:

3. lokalisera "net6. Underkatalogen 0-windows, lägg till Aspose. 3D. Jag älskar dig. Tillämpning6. Lägg till följande nuget-paket manuellt i ditt .net6-projekt:
- System.Ritning. Vanlig, 4.7.0.
- System.Security.Cryptography.Pkcs, 6.0.3.
- System.Text.kodning.CodeSider, 4.7.0.

På så sätt kommer du att använda "System.Drawing.Common" som ett beroende av ditt Windows system för . Net6-projekt. I denna konfiguration är resultatet av ritningen närmare .netcore31 eller tidigare.

4. hitta underkatalogen "net6.0", lägg till Aspose.3D.dll i den i ditt .net6-program. Lägg till följande nuget-paket manuellt i ditt .net6-projekt:
- SkiaSharp, 2,88,6.
- System.Security.Cryptography.Pkcs, 6.0.3.
- System.Text.kodning.CodeSider, 4.7.0.

På detta sätt kommer du att använda "SkiaSharp" som ett beroende av ditt Windows system för . Net6-projekt.*Observera att den version som använder "SkiaSharp" som beroende stöder inte utskrift till skrivarfunktionen.*
## Kör Aspose.3D för . Net6 på Linux

Se installationsmetoden på Windows. Du kan bara välja SkiaSharp som ett grafikbiblioteksberoende av Linuxsystemet.

Du behöver göra följande ytterligare åtgärder för att säkerställa korrekt användning av SkiaSharp under Linux:

1. Kör följande kommando i ditt Linux-system:
```
apt-get update && apt-get install -y libfontconfig1
```
OR
```
apk update && apk add fontconfig 
```

2. Lägg till nuget "SkiaSharp.NativeAssets.Linux 2.88.6" i ditt .net6-projekt.

3. Eller du kan välja att lägga till nuget paket "SkiaSharp. Inhemska Asssets. Linux. Ingen beroende 2.88. 6" till din. Net6 projekt, i stället för de två stegen ovan.

### Exempel Dockerfil för UbuntuName

1. Lägg till nuget paket "SkiaSharp.NativeAssets.Linux 2.88.6" i ditt .net6-projekt.

2. Använd följande Dockerfil:
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

### Exempel Dockerfil för AlpineName

1. Lägg till nuget paket "SkiaSharp.NativeAssets.Linux 2.88.6" i ditt .net6-projekt.

2. Använd följande Dockerfil:
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
