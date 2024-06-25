---
title: Systemkrav
type: docs
weight: 50
url: /sv/python-net/system-requirements/
description: Systemkrav för Aspose.3D for Python via .NET.
---
##  **Översikt**
` `Att bygga och manipulera dokumentformat för 3D, datorn som Aspose.3D for Python via .NET kör på behöver inte ha modellerings- och renderingsprogram installerad. Aspose.3D for Python via .NET API innehåller också dokumentgenereringsmotor.
##  **Stödda operativsystem**
Aspose.3D for Python via .NET stöder operativsystemet 64-bitars eller 32-bitars där Python 3.5 eller senare är installerat.

<table>  
    <tr>
        <td style="font-weight: bold; width:400px">Operativsystem</td>
        <td style="font-weight: bold; width:400px">Versioner</td>
    </tr>
    <tr>
        <td>Microsoft Windows</td>
        <td>
            <ul>
                <li>Windows 2003-server (x64, x86)</li>
                <li>Windows 2008-server (x64, x86)</li>
                <li>Windows 2012-server (x64, x86)</li>
                <li>Windows 2012 R2-server (x64, x86)</li>
                <li>Windows 2016-server (x64, x86)</li>
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
        <td>LinuxName</td>
        <td>
            <ul>
                <li>UbuntuName</li>
                <li>OpenSUSEName</li>
                <li>CentOS</li>
                <li>Och andra</li>
            </ul>
        </td>
    </tr>
</table>


## Systemkrav för Target Linux-plattformar

- GCC-6 körtidsbibliotek (eller senare).
  
- [`libgdiplus`](https://github.com/mono/libgdiplus): an öppen källkodimplementering av GDI API.

- Beroenden för .NET Core Runtime. Installera .NET kärnan körning i sig krävs INTE.

- For Python 3.5-3.7: The `pymalloc` build of Python is needed. The `--with-pymalloc` Python build option is enabled by default. Typically, the `pymalloc` build of Python is marked with `m` suffix in the filename.

- `libpython` shared Python library. The `--enable-shared` Python build option is disabled by default, some Python distributions do not contain the `libpython` shared library. For some linux platforms, the `libpython` shared library can be installed using the package manager, for example: `sudo apt-get install libpython3.7`. The common issue is that `libpython` library is installed in a different location than the standard system location for shared libraries. The issue can be fixed by using the Python build options to set alternate library paths when compiling Python, or fixed by creating a symbolic link to the `libpython` library file in the system standard location for shared libraries. Typically, the `libpython` shared library file name is `libpythonX.Ym.so.1.0` for Python 3.5-3.7, or `libpythonX.Y.so.1.0` for Python 3.8 or later (for example: libpython3.7m.so.1.0, libpython3.9.so.1.0).



Dessutom kan alla operativsystem som kan installera Mono(.NET 4.0 Ramstöd) eller använda .NET kärna använda Aspose.3D for Python via .NET.
##  **Redigera**
###  **Vulkan Ordförande**
Aspose.3D for Python via .NET kräver Vulkan x64-plattform, x86 stöds inte.

- AMD Radeon 7700 serien och nyare
- NVIDIA GeForce 600-serien och nyare
- Intel Skylake och nyare
