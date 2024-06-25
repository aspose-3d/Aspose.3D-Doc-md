---
title: Sistem gereksinimleri
type: docs
weight: 50
url: /tr/python-net/system-requirements/
description: The system requirements for the Aspose.3D for Python via .NET.
---
##  **Overview**
` `To build and manipulate 3D document formats, the machine that Aspose.3D for Python via .NET runs on doesn't need to have modeling and rendering software installed. Aspose.3D for Python via .NET API also incorporates document generation engine.
##  **Orted upported ating perating stem ystem**
Aspose.3D for Python via .NET supports any 64-bit or 32-bit operating system where Python 3.5 or later is installed.

<table>  
    <tr>
        <td style="font-weight: bold; width:400px">Ating perating stem ystem</td>
        <td style="font-weight: bold; width:400px">Versions</td>
    </tr>
    <tr>
        <td>Microsoft Windows</td>
        <td>
            <ul>
                <li>Windows 2003 sunucu (x64, x86)</li>
                <li>Windows 2008 sunucusu (x64, x86)</li>
                <li>Windows 2012 sunucusu (x64, x86)</li>
                <li>Windows 2012 r2 sunucusu (x64, x86)</li>
                <li>Windows 2016 sunucu (x64, x86)</li>
                <li>Windows 2019 sunucusu (x64, x86)</li>
                <li>Windows xp (x64, x86)</li>
                <li>Windows vista (x64, x86)</li>
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
                <li>OpenpenUE E</li>
                <li>CentenS</li>
                <li>Ve diğerleri</li>
            </ul>
        </td>
    </tr>
</table>


## Target Linux latlatform için System equiequiequi

- GCC-6 çalışma zamanı kütüphaneleri (veya üstü).
  
- [`libgdiplus`](https://github.com/mono/libgdiplus): gdi API 'nin açık kaynak uygulaması.

- Dependencies of .NET Core Runtime. Installing .NET Core Runtime itself is NOT required.

- For Python 3.5-3.7: The `pymalloc` build of Python is needed. The `--with-pymalloc` Python build option is enabled by default. Typically, the `pymalloc` build of Python is marked with `m` suffix in the filename.

- `libpython` shared Python library. The `--enable-shared` Python build option is disabled by default, some Python distributions do not contain the `libpython` shared library. For some linux platforms, the `libpython` shared library can be installed using the package manager, for example: `sudo apt-get install libpython3.7`. The common issue is that `libpython` library is installed in a different location than the standard system location for shared libraries. The issue can be fixed by using the Python build options to set alternate library paths when compiling Python, or fixed by creating a symbolic link to the `libpython` library file in the system standard location for shared libraries. Typically, the `libpython` shared library file name is `libpythonX.Ym.so.1.0` for Python 3.5-3.7, or `libpythonX.Y.so.1.0` for Python 3.8 or later (for example: libpython3.7m.so.1.0, libpython3.9.so.1.0).



Furthermore, any operating system that can install Mono(.NET 4.0 Framework support) or use .NET core can use Aspose.3D for Python via .NET.
##  **Rendering**
###  **Vulkan**
Aspose.3D for Python via .NET vulkan x64 platformunu gerektirir, x86 desteklenmez.

- AMD adeadeon 7700 serisi ve daha yeni
- NV600 600 600 600 600 eForce 600 serisi ve daha yeni
- Intel Skylake ve daha yeni
