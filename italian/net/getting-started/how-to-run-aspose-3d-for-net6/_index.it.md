---
title: Come eseguire Aspose.3D per. Net6
type: docs
description: Come eseguire Aspose.3D per. Net6
weight: 138
url: /it/net/how-to-run-aspose-3d-for-net6/
---
## Panoramica

Per il. Le piattaforme NET6 (o successive), confrontate con le piattaforme precedenti (.netcore31 o prima), una differenza importante riguarda la libreria grafica.
In questo ufficiale [Documento Microsoft](https://learn.microsoft.com/en-gb/dotnet/core/compatibility/core-libraries/6.0/system-drawing-common-windows-only), si spiega per. NET6 o versioni successive la libreria grafica "System.Drawing.Common" sarà supportata solo su Windows e fornisce consigli per sostituire la libreria grafica.

Per il prodotto Apose.3D, abbiamo condotto la valutazione e abbiamo completato la migrazione della libreria grafica. Usiamo SkiaSharp invece di System.Drawing. Comune in sistemi non Windows, come suggerito nella documentazione ufficiale di Microsoft. Tieni presente che questa modifica critica avrà effetto tra Aspose.3D 22.10.1 o successiva per. Net6.

Per. netcore31 o prima, per compatibilità e stabilità, attualmente utilizziamo ancora la libreria grafica "System.Drawing.Common". Le dipendenze per. netcore31 o before sono le seguenti:
- Sistema. Disegno. Comune, 4.7.0.
- Sistema. Sicurezza. Crittografia. Pkcs, 5.0.1.
- Sistema. Testo. Codifica. CodePages, 4.7.0.

## Esegui Aspose.3D per. Net6 su Windows

Per prima cosa puoi creare un'applicazione. net6 con VS2022, quindi puoi scegliere le seguenti opzioni di installazione:

### Installare tramite nuget

1. Cerca Aspose.3D da NuGet: [Aspose. Pacchetto 3D for .NET NuGet](https://www.nuget.org/packages/Aspose.3D/).
Puoi anche installare Aspose.3D dal gestore di pacchetti Nuget in VS2022.

2. "SkiaSharp" o "System.Drawing.Common" verranno installati automaticamente come dipendenza di Aspose.3D 22.10.1 o successiva per. Piattaforme Net6, che dipende dalla configurazione "Target OS" nel tuo progetto.
- Imposta il "Sistema operativo Target" su "Windows" per il tuo progetto, userai "System.Drawing.Common" come dipendenza dal tuo sistema Windows per. Progetto Net6. In questa configurazione, il risultato del disegno è più vicino a. netcore31 o prima.
**! [Obiettivo Config OS] (TargetOS.png)**
- Imposta il "sistema operativo Target" su "Nessuno" o altre opzioni per il tuo progetto, utilizzerai "SkiaSharp" come dipendenza dal tuo sistema Windows per. Progetto Net6.*Si prega di notare che la versione che utilizza "SkiaSharp" come dipendenza non supporta la stampa alla funzione stampante.*

### Installare tramite msi o DLL

1. [Scarica Aspose.3D.msi o DLL](https://releases.aspose.com/3d/net/)

2. Apri la directory di installazione o la directory DLL, quindi seleziona il passaggio 3 o 4 di seguito:

3. Individua la sottodiana "net6.0-windows", aggiungi Aspose.3D.dll alla tua applicazione. net6. Aggiungi manualmente i seguenti pacchetti nuget al tuo progetto. net6:
- Sistema. Disegno. Comune, 4.7.0.
- Sicurezza del sistema. Crittografia. Pkcs, 6.0.3.
- Sistema. Testo. Codifica. CodePages, 4.7.0.

In questo modo, utilizzerai "System.Drawing.Common" come dipendenza dal tuo sistema Windows per. Progetto Net6. In questa configurazione, il risultato del disegno è più vicino a. netcore31 o prima.

4. Individua la sottoditrovano "net6.0", aggiungi Aspose.3D.dll alla tua applicazione. net6. Aggiungi manualmente i seguenti pacchetti nuget al tuo progetto. net6:
- SkiaSharp, 2.88.6.
- Sicurezza del sistema. Crittografia. Pkcs, 6.0.3.
- Sistema. Testo. Codifica. CodePages, 4.7.0.

In questo modo, utilizzerai "SkiaSharp" come dipendenza dal tuo sistema Windows per. Progetto Net6.*Si prega di notare che la versione che utilizza "SkiaSharp" come dipendenza non supporta la stampa alla funzione stampante.*
## Esegui Aspose.3D per. Net6 su Linux

Fare riferimento al metodo di installazione su Windows, è possibile selezionare SkiaSharp solo come dipendenza della libreria grafica dal sistema Linux.

È necessario eseguire le seguenti operazioni aggiuntive per garantire un uso corretto di SkiaSharp sotto Linux:

1. Esegui il seguente comando nel tuo sistema Linux:
```
apt-get update && apt-get install -y libfontconfig1
```
OR
```
apk update && apk add fontconfig 
```

2. Aggiungi i pacchetti nuget "SkiaSharp.NativeAssets.Linux 2.88.6" al tuo progetto. net6.

3. Oppure puoi scegliere di aggiungere nuget pacchetti "SkiaSharp.NativeAssets.Linux.NoDependencies 2.88.6" al tuo progetto. net6, invece dei due passaggi precedenti.

### Dockerfile di esempio per Ubuntu

1. Aggiungi i pacchetti nuget "SkiaSharp.NativeAssets.Linux 2.88.6" al tuo progetto. net6.

2. Usa il seguente Dockerfile:
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

### Esempio Dockerfile per Alpine

1. Aggiungi i pacchetti nuget "SkiaSharp.NativeAssets.Linux 2.88.6" al tuo progetto. net6.

2. Usa il seguente Dockerfile:
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
