---
title: So führen Sie Aspose aus. 3D für. Net6
type: docs
description: So führen Sie Aspose aus. 3D für. Net6
weight: 138
url: /de/net/how-to-run-aspose-3d-for-net6/
---
## Übersicht

Für die. NET6-Plattformen (oder später), im Vergleich zu früheren Plattformen (.netcore31 oder vorher), ein wichtiger Unterschied ist die Grafik bibliothek.
In diesem offiziellen [Microsoft Dokument](https://learn.microsoft.com/en-gb/dotnet/core/compatibility/core-libraries/6.0/system-drawing-common-windows-only) erklärt es für. NET6 oder höher ver öffentlicht die Grafik bibliothek "System.Drawing.Common" wird nur auf Windows unterstützt und gibt Empfehlungen zum Ersetzen der Grafik bibliothek.

Für das Produkt Apose.3D haben wir die Auswertung durchgeführt und die Migration der Grafik bibliothek abgeschlossen. Wir verwenden SkiaS harp anstelle von System.Drawing.Common in Nicht-Windows-Systemen, wie in der offiziellen Dokumentation von Microsoft vor geschlagen. Bitte beachten Sie, dass diese kritische Änderung in Aspose.3D 22.10.1 oder später für wirksam wird. Net6.

Für. netcore31 oder früher verwenden wir aus Gründen der Kompatibilität und Stabilität derzeit noch die Grafik bibliothek "System.Drawing.Common". Die Abhängigkeiten für. netcore31 oder früher sind wie folgt:
- System. Zeichnung. Common, 4.7.0.
- System. Sicherheit. Kryptographie. Pkcs, 5.0.1.
- System.Text. Codierung. CodePages, 4.7.0.

## Run Aspose.3D für. Net6 auf Windows

Zuerst können Sie eine. net6-Anwendung mit VS2022 erstellen, dann können Sie die folgenden Installation optionen auswählen:

### Installieren Sie über nuget

1. Suchen Sie nach Aspose.3D ab NuGet: [Aspose.3D for .NET NuGet Paket](https://www.nuget.org/packages/Aspose.3D/).
Sie können auch Aspose.3D aus dem Nuget-Paket manager in VS2022 installieren.

2. "SkiaS harp" oder "System.Drawing.Common" wird automatisch als Abhängigkeit von Aspose installiert. 3D 22.10.1 oder später für. Net6-Plattformen, die von der Konfiguration "Target OS" in Ihrem Projekt abhängen.
- Setzen Sie das "Target OS" auf "Windows" für Ihr Projekt. Sie verwenden "System.Drawing.Common" als Abhängigkeit von Ihrem Windows-System für. Net6-Projekt. In dieser Konfiguration ist das Ergebnis der Zeichnung näher an. netcore31 oder vorher.
**! [Konfig-Ziel OS] (TargetOS.png)**
- Setzen Sie das "Target OS" auf "Keine" oder andere Optionen für Ihr Projekt. Sie verwenden "SkiaS harp" als Abhängigkeit von Ihrem Windows-System für. Net6-Projekt.*Bitte beachten Sie, dass die Version, die "SkiaS harp" als Abhängigkeit verwendet, das Drucken auf Drucker funktion nicht unterstützt.*

### Installieren Sie über msi oder DLL

1. [Herunter laden Aspose.3D.msi oder DLL](https://releases.aspose.com/3d/net/)

2. Öffnen Sie das Installation verzeichnis oder das DLL-Verzeichnis und wählen Sie nachfolgend Schritt 3 oder 4 aus:

3. Suchen Sie das Unter verzeichnis "net 6.0-windows" und fügen Sie die Aspose.3D.dll zu Ihrer. net6-Anwendung hinzu. Fügen Sie Ihrem. net6-Projekt die folgenden nuget-Pakete manuell hinzu:
- System. Zeichnung. Common, 4.7.0.
- System. Sicherheit. Kryptographie. Pkcs, 6.0.3.
- System.Text. Codierung. CodePages, 4.7.0.

Auf diese Weise verwenden Sie "System.Drawing.Common" als Abhängigkeit von Ihrem Windows-System für. Net6-Projekt. In dieser Konfiguration ist das Ergebnis der Zeichnung näher an. netcore31 oder vorher.

4. Suchen Sie das Unter verzeichnis "net6.0" und fügen Sie die Aspose.3D.dll zu Ihrer. net6-Anwendung hinzu. Fügen Sie Ihrem. net6-Projekt die folgenden nuget-Pakete manuell hinzu:
- SkiaSharp, 2.88.6.
- System. Sicherheit. Kryptographie. Pkcs, 6.0.3.
- System.Text. Codierung. CodePages, 4.7.0.

Auf diese Weise verwenden Sie "SkiaS harp" als Abhängigkeit von Ihrem Windows-System für. Net6-Projekt.*Bitte beachten Sie, dass die Version, die "SkiaS harp" als Abhängigkeit verwendet, das Drucken auf Drucker funktion nicht unterstützt.*
## Run Aspose.3D für. Net6 auf Linux

Beziehen Sie sich auf die Installation methode unter Windows. Sie können SkiaS harp nur als Abhängigkeit der Grafik bibliothek vom Linux-System auswählen.

Sie müssen die folgenden zusätzlichen Operationen durchführen, um sicher zustellen, dass SkiaS harp unter Linux ordnungs gemäß verwendet wird:

1. Führen Sie den folgenden Befehl in Ihrem Linux-System aus:
```
apt-get update && apt-get install -y libfontconfig1
```
OR
```
apk update && apk add fontconfig 
```

2. Fügen Sie die nuget-Pakete "SkiaS harp.Native Assets.Linux 2.88.6" zu Ihrem. net6-Projekt hinzu.

3. Oder Sie können anstelle der beiden oben genannten Schritte die nuget-Pakete "SkiaS harp.Native Assets.Linux.NoDep enden cies 2.88.6" zu Ihrem. net6-Projekt hinzufügen.

### Beispiel Docker file für Ubuntu

1. Fügen Sie die nuget-Pakete "SkiaS harp.Native Assets.Linux 2.88.6" zu Ihrem. net6-Projekt hinzu.

2. Verwenden Sie die folgende Docker file:
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

### Beispiel Docker file für Alpine

1. Fügen Sie die nuget-Pakete "SkiaS harp.Native Assets.Linux 2.88.6" zu Ihrem. net6-Projekt hinzu.

2. Verwenden Sie die folgende Docker file:
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
