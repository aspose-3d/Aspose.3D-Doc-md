---
title: Requisitos del sistema
type: docs
weight: 50
url: /es/python-net/system-requirements/
description: Requisitos del sistema para el Aspose.3D for Python via .NET.
---
##  **Descripción general**
` ` Para construir y manipular los formatos de documentos 3D, la máquina en la que se ejecuta Aspose.3D for Python via .NET no necesita tener instalado software de modelado y renderizado. Aspose.3D for Python via .NET API también incorpora motor de generación de documentos.
##  **Sistema operativo compatible**
Aspose.3D for Python via .NET admite cualquier sistema operativo de 64 o 32 bits en el que esté instalado Python 3,5 o posterior.

<table>  
    <tr>
        <td style="font-weight: bold; width:400px">Sistema operativo</td>
        <td style="font-weight: bold; width:400px">Versiones</td>
    </tr>
    <tr>
        <td>Microsoft Windows</td>
        <td>
            <ul>
                <li>Windows 2003 Server (x64, x86)</li>
                <li>Windows 2008 Server (x64, x86)</li>
                <li>Windows 2012 Server (x64, x86)</li>
                <li>Windows 2012 R2 Server (x64, x86)</li>
                <li>Servidor Windows 2016 (x64, x86)</li>
                <li>Windows Servidor 2019 (x64, x86)</li>
                <li>Windows XP (x64, x86)</li>
                <li>Windows Vista (x64, x86)</li>
                <li>Windows 7 (x64, x86)</li>
                <li>Windows 8, 8,1 (x64, x86)</li>
                <li>Windows 10 (x64, x86)</li>
            </ul>
        </td>
    </tr>
    <tr>
        <td>Linux</td>
        <td>
            <ul>
                <li>Ubuntu</li>
                <li>Abridor</li>
                <li>CentOS</li>
                <li>Y otros</li>
            </ul>
        </td>
    </tr>
</table>


## Requisitos del sistema para la plataforma Target Linux

- GCC-6 bibliotecas en tiempo de ejecución (o posteriores).
  
- [`libgdiplus`](https://github.com/mono/libgdiplus): una implementación de código abierto del GDI API.

- Dependencias de .NET Core Runtime. La instalación de .NET Core Runtime NO es necesaria.

- Para Python 3.5-3.7: Se necesita la construcción `pymalloc` de Python. La opción de compilación `--with-pymalloc` Python está habilitada por defecto. Por lo general, la construcción `pymalloc` de Python está marcada con el sufijo `m` en el nombre de archivo.

- Biblioteca `libpython` compartida Python. La opción de compilación `--enable-shared` Python está deshabilitada de forma predeterminada, algunas distribuciones Python no contienen la biblioteca compartida `libpython`. Para algunas plataformas Linux, la biblioteca compartida `libpython` se puede instalar usando el administrador de paquetes, por ejemplo: `sudo apt-get install libpython3.7`. El problema común es que la biblioteca `libpython` se instala en una ubicación diferente a la ubicación estándar del sistema para las bibliotecas compartidas. El problema puede solucionarse utilizando las opciones de compilación de Python para establecer rutas de biblioteca alternativas al compilar Python, o solucionarse creando un vínculo simbólico al archivo de biblioteca `libpython` en la ubicación estándar del sistema para bibliotecas compartidas. Normalmente, el nombre del archivo de biblioteca compartida `libpython` es `libpythonX.Ym.so.1.0` para Python 3.5-3.7, o `libpythonX.Y.so.1.0` para Python 3,8 o posterior (por ejemplo: libpython3.7m.so.1.0, libpython3.9.so. 1,0).



Además, cualquier sistema operativo que pueda instalar Mono(.NET 4,0 Framework support) o usar .NET core puede usar Aspose.3D for Python via .NET.
##  **Rendering**
###  **Vulkan**
Aspose.3D for Python via .NET requiere la plataforma Vulkan x64, x86 no es compatible.

- AMD Radeon serie 7700 y más recientes
- Serie NVIDIA GeForce 600 y más reciente
- Intel Skylake y más nuevos
