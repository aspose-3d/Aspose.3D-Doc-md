---
title: System Anforderungen
type: docs
weight: 50
url: /de/python-net/system-requirements/
description: Die Systema forderungen für die Aspose.3D für Python via .NET.
---
## **Übersicht**
` `Um 3D Dokument formate zu erstellen und zu bearbeiten, muss auf dem Computer, auf dem Aspose.3D für Python via .NET ausgeführt wird, keine Modellierungs-und Rendering-Software installiert sein. Aspose.3D für Python via .NET API enthält auch einen Motor der Dokumenten generation.
## **Unterstütztes Betriebs system**
Aspose.3D für Python via .NET unterstützt jedes 64-Bit-oder 32-Bit-Betriebssystem, bei dem Python 3.5 oder höher installiert ist.

<table>  
    <tr>
        <td style="font-weight: bold; width:400px">Betriebs system</td>
        <td style="font-weight: bold; width:400px">Versionen</td>
    </tr>
    <tr>
        <td>Microsoft Windows</td>
        <td>
            <ul>
                <li>Windows 2003 Server (x64, x86)</li>
                <li>Windows 2008 Server (x64, x86)</li>
                <li>Windows 2012 Server (x64, x86)</li>
                <li>Windows 2012 R2 Server (x64, x86)</li>
                <li>Windows 2016 Server (x64, x86)</li>
                <li>Windows 2019 Server (x64, x86)</li>
                <li>Windows XP (x64, x86)</li>
                <li>Windows Vista (x64, x86)</li>
                <li>Windows 7 (x64, x86)</li>
                <li>Windows 8, 8.1 (x64, x86)</li>
                <li>Windows 10 (x64, x86)</li>
            </ul>
        </td>
    </tr>
    <tr>
        <td>Linux</td>
        <td>
            <ul>
                <li>Ubuntu</li>
                <li>OpenSUSE</li>
                <li>CentOS</li>
                <li>Und andere</li>
            </ul>
        </td>
    </tr>
</table>


## System voraussetzungen für Target Linux Platform

- GCC-6 Laufzeit bibliotheken (oder später).
  
- [`libgdiplus`](https://github.com/mono/libgdiplus): eine Open-Source-Implementierung des GDI API.

- Abhängigkeiten von .NET Core Runtime. Die Installation von .NET Core Runtime selbst ist NICHT erforderlich.

- Für Python 3, 5-3, 7: Der Bau `pymalloc` der Python wird benötigt. Die Build-Option `--with-pymalloc` Python ist standard mäßig aktiviert. In der Regel ist der Build `pymalloc` von Python im Dateinamen mit dem Suffix `m` gekennzeichnet.

- `libpython` teilte Python Bibliothek. Die Build-Option `--enable-shared` Python ist standard mäßig deaktiviert. Einige Python-Distributionen enthalten nicht die gemeinsam genutzte Bibliothek `libpython`. Für einige Linux-Plattformen kann die gemeinsam genutzte Bibliothek `libpython` mit dem Paket manager installiert werden, zum Beispiel: `sudo apt-get install libpython3.7`. Das häufige Problem ist, dass die Bibliothek `libpython` an einem anderen Ort als der Standard-Systemst andort für gemeinsam genutzte Bibliotheken installiert ist. Das Problem kann behoben werden, indem die Build-Optionen Python verwendet werden, um alternative Bibliotheks pfade beim Kompilieren von Python festzulegen, oder indem eine symbolische Verknüpfung zur Bibliotheks datei `libpython` im Systemstandard-Speicherort für gemeinsam genutzte Bibliotheken erstellt wird. In der Regel lautet der Dateiname der gemeinsam genutzten Bibliothek `libpython` für Python 3.5-3, 7 oder `libpythonX.Y.so.1.0` für Python 3.8 oder höher (z. B.: libpython 3.7m.so.1.0, libpython3.9.so.1.0).



Darüber hinaus kann jedes Betriebs system, das Mono(.NET 4.0 Framework-Unterstützung) installieren oder .NET core verwenden kann, Aspose.3D für Python via .NET verwenden.
## **Rendering**
### **Vulkan**
Aspose.3D für Python via .NET erfordert Vulkan x64 Plattform, x86 wird nicht unterstützt.

- AMD Radeon 7700 Serie und neuer
- NVIDIA GeForce 600 Serie und neuer
- Intel Skylake und neuere
