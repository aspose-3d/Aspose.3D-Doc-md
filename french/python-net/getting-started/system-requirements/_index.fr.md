---
title: Configuration requise
type: docs
weight: 50
url: /fr/python-net/system-requirements/
description: Les exigences du système pour le Aspose.3D pour Python via .NET.
---
## **Aperçu**
` `Pour créer et manipuler les formats de documents 3D, la machine sur laquelle s'exécute Aspose.3D pour Python via .NET n'a pas besoin d'installer un logiciel de modélisation et de rendu. Aspose.3D pour Python via .NET API intègre également un moteur de génération de document.
## **Système d'exploitation pris en charge**
Aspose.3D pour Python via .NET prend en charge n'importe quel système d'exploitation 64 bits ou 32 bits où Python 3.5 ou version ultérieure est installé.

<table>  
    <tr>
        <td style="font-weight: bold; width:400px">Système d'exploitation</td>
        <td style="font-weight: bold; width:400px">Versions</td>
    </tr>
    <tr>
        <td>Microsoft Windows</td>
        <td>
            <ul>
                <li>Windows 2003 Serveur (x64, x86)</li>
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


## Exigences système pour la plate-forme cible Linux

- GCC-6 les bibliothèques d'exécution (ou plus tard).
  
- [`libgdiplus`](https://github.com/mono/libgdiplus): une implémentation Open Source du GDI API.

- Dépendances du .NET Core Runtime. L'installation du .NET Core Runtime n'est PAS requise.

- Pour Python 3.5-3.7: La construction `pymalloc` de Python est nécessaire. L'option de construction `--with-pymalloc` Python est activée par défaut. En règle générale, la version `pymalloc` de Python est marquée avec le suffixe `m` dans le nom de fichier.

- `libpython` a partagé la bibliothèque Python. L'option de construction `--enable-shared` Python est désactivée par défaut, certaines distributions Python ne contiennent pas la bibliothèque partagée `libpython`. Pour certaines plates-formes Linux, la bibliothèque partagée `libpython` peut être installée à l'aide du gestionnaire de packages, par exemple: `sudo apt-get install libpython3.7`. Le problème courant est que la bibliothèque `libpython` est installée dans un emplacement différent de l'emplacement système standard pour les bibliothèques partagées. Le problème peut être résolu en utilisant les options de construction Python pour définir des chemins de bibliothèque alternatifs lors de la compilation de Python, ou en créant un lien symbolique vers le fichier de la bibliothèque `libpython` dans l'emplacement standard du système pour les bibliothèques partagées. En règle générale, le nom de fichier de bibliothèque partagé `libpython` est `libpythonX.Ym.so.1.0` pour Python 3.5-3.7, ou `libpythonX.Y.so.1.0` pour Python 3.8 ou version ultérieure (par exemple: libpython3.7m.so.1.0, libpython3.9.so.1.0).



De plus, tout système d'exploitation pouvant installer Mono (support .NET 4.0 Framework) ou utiliser le cœur .NET peut utiliser le Aspose.3D pour Python via .NET.
## **Rendu**
### **Vulkan**
Aspose.3D pour Python via .NET nécessite la plate-forme Vulkan x64, x86 n'est pas pris en charge.

- Série AMD Radeon 7700 et plus récente
- Série NVIDIA GeForce 600 et plus récente
- Intel Skylake et plus récent
