---
title: Exigences système
type: docs
weight: 50
url: /fr/python-net/system-requirements/
description: La configuration système requise pour le Aspose.3D for Python via .NET.
---
##  **Aperçu**
` ` Pour construire et manipuler les formats de document 3D, la machine sur laquelle Aspose.3D for Python via .NET tourne n'a pas besoin d'avoir un logiciel de modélisation et de rendu installé. Aspose.3D for Python via .NET API intègre également le moteur de génération de documents.
##  **Système d'exploitation pris en charge**
Aspose.3D for Python via .NET prend en charge tout système d'exploitation 64 bits ou 32 bits sur lequel Python 3.5 ou une version ultérieure est installé.

<table>  
    <tr>
        <td style="font-weight: bold; width:400px">Système d'exploitation</td>
        <td style="font-weight: bold; width:400px">Versions</td>
    </tr>
    <tr>
        <td>Microsoft Windows</td>
        <td>
            <ul>
                <li>Serveur Windows 2003 (x64, x86)</li>
                <li>Windows 2008 Serveur (x64, x86)</li>
                <li>Windows 2012 Serveur (x64, x86)</li>
                <li>Windows 2012 R2 Serveur (x64, x86)</li>
                <li>Windows 2016 Serveur (x64, x86)</li>
                <li>Windows 2019 Serveur (x64, x86)</li>
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
                <li>Et d'autres</li>
            </ul>
        </td>
    </tr>
</table>


## Exigences système pour la plate-forme Linux cible

- GCC-6 les bibliothèques d'exécution (ou plus tard).
  
- [`libgdiplus`](https://github.com/mono/libgdiplus): une implémentation Open Source de GDI API.

- Dépendances de .NET Core Runtime. L'installation de .NET Core Runtime elle-même n'est PAS nécessaire.

- Pour Python 3.5-3.7: La build `pymalloc` de Python est nécessaire. L'option de build `--with-pymalloc` Python est activée par défaut. En règle générale, la construction `pymalloc` de Python est marquée avec le suffixe `m` dans le nom du fichier.

- `libpython` bibliothèque partagée Python. L'option de build `--enable-shared` Python est désactivée par défaut, certaines distributions Python ne contiennent pas la bibliothèque partagée `libpython`. Pour certaines plates-formes Linux, la bibliothèque partagée `libpython` peut être installée en utilisant le gestionnaire de paquets, par exemple: `sudo apt-get install libpython3.7`. Le problème commun est que la bibliothèque `libpython` est installée dans un emplacement différent de l'emplacement système standard pour les bibliothèques partagées. Le problème peut être résolu en utilisant les options de construction Python pour définir des chemins de bibliothèque alternatifs lors de la compilation Python, ou en créant un lien symbolique vers le fichier de bibliothèque `libpython` dans l'emplacement standard du système pour les bibliothèques partagées. Typiquement, le nom de fichier de la bibliothèque partagée `libpython` est `libpythonX.Ym.so.1.0` pour Python 3.5-3.7, ou `libpythonX.Y.so.1.0` pour Python 3.8 ou plus (par exemple: libpython3.7m.so.1.0, libpython3.9.so.1.0).



De plus, tout système d'exploitation capable d'installer Mono(support du Framework .NET 4.0) ou d'utiliser .NET core peut utiliser Aspose.3D for Python via .NET.
##  **Rendu**
###  **Vulkan**
Aspose.3D for Python via .NET nécessite la plate-forme Vulkan x64, x86 n'est pas pris en charge.

- Série AMD Radeon 7700 et plus récente
- Série NVIDIA GeForce 600 et plus récente
- Intel Skylake et plus récent
