---
title: Systemkrav
type: docs
weight: 50
url: /sv/python-net/system-requirements/
description: Systemkrav för Aspose.3D för Python via .NET.
---
## **Översikt**
` `Att bygga och manipulera 3D dokumentformat, Den maskin som Aspose.3D för Python via .NET körs på behöver inte ha modell- och renderingsprogram installerad. Aspose.3D för Python via .NET API innehåller också dokumentgenereringsmotor.
## **Stödda operativsystem**
Aspose.3D för Python via .NET stöder ett 64-bitars eller 32-bitars operativsystem där Python 3.5 eller senare är installerat ..

<table>  
    <tr>
        <td style="font-weight: bold; width:400px">Operativsystem</td>
        <td style="font-weight: bold; width:400px">Versioner</td>
    </tr>
    <tr>
        <td>Microsoft Windows</td>
        <td>
            <ul>
                <li>Windows 2003- server (x64, x86)</li>
                <li>Windows 2008- server (x64, x86)</li>
                <li>Windows 2012- server (x64, x86)</li>
                <li>Windows 2012 R2-server (x64, x86)</li>
                <li>Windows 2016-server (x64, x86)</li>
                <li>Windows 2019- server (x64, x86)</li>
                <li>Windows XP (x64, x86)</li>
                <li>Windows Vista (x64, x86)</li>
                <li>Windows 7 (x64, x86)</li>
                <li>Windows 8, 1 (x64, x86)</li>
                <li>Windows 10 (x64, x86)</li>
            </ul>
        </td>
    </tr>
    <tr>
        <td>Linux</td>
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


## Systemkrav för mål Linux

- GCC-6 körtidsbibliotek (eller senare).
  
- [`libgdiplus`](https://github.com/mono/libgdiplus): Genomförande av GDI API.

- Beroende på .NET Core Runtime. Installera .NET Core Runtime själv krävs INTE.

- För Python 3,5-3.7: Den `pymalloc`-byggnaden av Python behövs. `--with-pymalloc` Python byggnadsalternativet är aktiverat som standard. Typiskt är `pymalloc`-bygget av Python markerat med `m`-suppsättning i filnamnet.

- `libpython` gemensamt Python bibliotek. `--enable-shared` Python byggnadsalternativet är inaktiverat som standard, Python distributioner innehåller inte det gemensamma biblioteket `libpython`. För vissa linuxplattformar kan det delade biblioteket `libpython` installeras med pakethanteraren, till exempel: `sudo apt-get install libpython3.7`. Den vanliga frågan är att `libpython` bibliotek är installerat på en annan plats än standardsystemplatsen för delade bibliotek. Problemet kan rättas genom att använda Python byggnadsalternativ för att ställa in alternativa bibliotekssökvägar vid kompilering . Python, eller fixeras genom att skapa en symbolisk länk till biblioteksfilen `libpython` i systemets standardplats för delade bibliotek. Typiskt är `libpython`-filnamnet `libpythonX.Ym.so.1.0` för Python 3.5-3. 7 eller `libpythonX.Y.so.1.0` för Python 3,8 eller senare (t.ex. libpython3.7m. Så... 1. - Libpython3.9. Så... 1. ).



Dessutom, något operativsystem som kan installera Mono(.NET 4.0 Ramstöd) eller använda .NET kärna kan använda Aspose.3D för Python via .NET.
## **Redigera**
### **Vulkan Ordförande**
Aspose.3D för Python via .NET kräver Vulkan x64-plattform, x86 stöds inte.

- AMD Radeon 7700 serien och nyare
- NVIDIA GeForce 600-serien och nyare
- Intel Skylake och nyare
