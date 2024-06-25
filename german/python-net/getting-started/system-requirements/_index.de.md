---
title: Systema forderungen
type: docs
weight: 50
url: /de/python-net/system-requirements/
description: Die Systema forderungen für Aspose.3D for Python via .NET.
---
##  **Übersicht**
` ` Um 3D Dokument formate zu erstellen und zu bearbeiten, muss auf dem Computer, auf dem Aspose.3D for Python via .NET ausgeführt wird, keine Modellierungs-und Rendering software installiert sein. Aspose.3D for Python via .NET API enthält auch die Dokument generierung Engine.
##  **Unterstütztes Betriebs system**
Aspose.3D for Python via .NET unterstützt jedes 64-Bit-oder 32-Bit-Betriebssystem, auf dem Python 3.5 oder höher installiert ist.

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
                <li>Windows Server 2008 (x64, x86)</li>
                <li>Windows Server 2012 (x64, x86)</li>
                <li>Windows 2012 R2 Server (x64, x86)</li>
                <li>Windows Server 2016 (x64, x86)</li>
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

- Für Python 3.5-3.7: Der `pymalloc`-Build von Python wird benötigt. Die Build-Option `--with-pymalloc` Python ist standard mäßig aktiviert. In der Regel ist der `pymalloc`-Build von Python im Dateinamen mit dem Suffix `m` gekennzeichnet.

- `libpython` shared Python library. The `--enable-shared` Python build option is disabled by default, some Python distributions do not contain the `libpython` shared library. For some linux platforms, the `libpython` shared library can be installed using the package manager, for example: `sudo apt-get install libpython3.7`. The common issue is that `libpython` library is installed in a different location than the standard system location for shared libraries. The issue can be fixed by using the Python build options to set alternate library paths when compiling Python, or fixed by creating a symbolic link to the `libpython` library file in the system standard location for shared libraries. Typically, the `libpython` shared library file name is `libpythonX.Ym.so.1.0` for Python 3.5-3.7, or `libpythonX.Y.so.1.0` for Python 3.8 or later (for example: libpython3.7m.so.1.0, libpython3.9.so.1.0).



Darüber hinaus kann jedes Betriebs system, das Mono(.NET 4.0 Framework-Unterstützung) installieren oder .NET Kern verwenden kann, Aspose.3D for Python via .NET verwenden.
##  **Rendering**
###  **Vulkan**
Aspose.3D for Python via .NET erfordert Vulkan x64 Plattform, x86 wird nicht unterstützt.

- AMD Radeon 7700 Serie und neuer
- NVIDIA GeForce 600 Serie und neuer
- Intel Skylake und neuere
