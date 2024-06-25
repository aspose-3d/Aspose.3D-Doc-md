---
title: Requisiti di sistema
type: docs
weight: 50
url: /it/python-net/system-requirements/
description: I requisiti di sistema per Aspose.3D for Python via .NET.
---
##  **Panoramica**
` ` Per creare e manipolare i formati di documenti 3D, la macchina su cui vengono eseguito Aspose.3D for Python via .NET non ha bisogno di avere installato il software di modellazione e rendering. Aspose.3D for Python via .NET API incorpora anche il motore di generazione dei documenti.
##  **Sistema operativo supportato**
Aspose.3D for Python via .NET supporta qualsiasi sistema operativo a 64 o 32 bit in cui è installato Python 3.5 o versioni successive.

<table>  
    <tr>
        <td style="font-weight: bold; width:400px">Sistema operativo</td>
        <td style="font-weight: bold; width:400px">Versioni</td>
    </tr>
    <tr>
        <td>Microsoft Windows</td>
        <td>
            <ul>
                <li>Server Windows 2003 (x64, x86)</li>
                <li>Server Windows 2008 (x64, x86)</li>
                <li>Server Windows 2012 (x64, x86)</li>
                <li>Server R2 Windows 2012 (x64, x86)</li>
                <li>Server Windows 2016 (x64, x86)</li>
                <li>Server Windows 2019 (x64, x86)</li>
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
                <li>E altri</li>
            </ul>
        </td>
    </tr>
</table>


## Requisiti di sistema per la piattaforma Linux di destinazione

- GCC-6 librerie di runtime (o successive).
  
- [`libgdiplus`](https://github.com/mono/libgdiplus): un'implementazione Open Source di GDI API.

- Dipendenze di .NET Core Runtime. L'installazione di .NET Core Runtime non è necessaria.

- Per Python 3.5-3.7: È necessaria la build `pymalloc` di Python. L'opzione di build `--with-pymalloc` Python è abilitata per impostazione predefinita. In genere, la build `pymalloc` di Python è contrassegnata con il suffisso `m` nel nome file.

- `libpython` ha condiviso la libreria Python. L'opzione di build `--enable-shared` Python è disabilitata per impostazione predefinita, alcune distribuzioni Python non contengono la libreria condivisa `libpython`. Per alcune piattaforme Linux, la libreria condivisa `libpython` può essere installata utilizzando il gestore pacchetti, ad esempio: `sudo apt-get install libpython3.7`. Il problema comune è che la libreria `libpython` è installata in una posizione diversa rispetto alla posizione di sistema standard per le librerie condivise. Il problema può essere risolto utilizzando le opzioni di build Python per impostare percorsi di libreria alternativi durante la compilazione di Python o risolto creando un collegamento simbolico al file di libreria `libpython` nella posizione standard di sistema per le librerie condivise. In genere, il nome del file della libreria condivisa `libpython` è `libpythonX.Ym.so.1.0` per Python 3.5-3.7 o `libpythonX.Y.so.1.0` per Python 3.8 o successivi (ad esempio: libpython3.7m.so.1.0, libpython3.9.so.1.0).



Inoltre, qualsiasi sistema operativo che può installare Mono(.NET 4.0 supporto Framework) o utilizzare .NET core può utilizzare Aspose.3D for Python via .NET.
##  **Rendering**
###  **Vulkan**
Aspose.3D for Python via .NET richiede la piattaforma Vulkan x64, x86 non è supportato.

- AMD Radeon serie 7700 e più recente
- NVIDIA GeForce 600 serie e più recente
- Intel Skylake e più recenti
