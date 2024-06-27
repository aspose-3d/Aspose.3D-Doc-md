---
title: Системные требования
type: docs
weight: 50
url: /ru/python-net/system-requirements/
description: Системные требования для Aspose.3D for Python via .NET.
---
##  **Обзор**
` ` Чтобы создавать и обрабатывать форматы документов 3D, на машине, на которой работает Aspose.3D for Python via .NET, не нужно устанавливать программное обеспечение для моделирования и рендеринга. Aspose.3D for Python via .NET API также включает механизм генерации документов.
##  **Поддерживаемая операционная система**
Aspose.3D for Python via .NET поддерживает любую 64-битную или 32-битную операционную систему, в которой установлена Python 3,5 или более поздняя.

<table>  
    <tr>
        <td style="font-weight: bold; width:400px">Операционная система</td>
        <td style="font-weight: bold; width:400px">Версии</td>
    </tr>
    <tr>
        <td>Microsoft Windows</td>
        <td>
            <ul>
                <li>Windows 2003 Сервер (x64, x86)</li>
                <li>Windows 2008 Сервер (x64, x86)</li>
                <li>Windows 2012 Сервер (x64, x86)</li>
                <li>Windows 2012 R2 Сервер (x64, x86)</li>
                <li>Windows 2016 Сервер (x64, x86)</li>
                <li>Windows 2019 Сервер (x64, x86)</li>
                <li>Windows XP (x64, x86)</li>
                <li>Windows Vista (x64, x86)</li>
                <li>Windows 7 (x64, x86)</li>
                <li>Windows 8, 1 (64, 86)</li>
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
                <li>ЦентОС</li>
                <li>И другие</li>
            </ul>
        </td>
    </tr>
</table>


## Требования к системе для Target Linux Platform

- GCC-6 библиотеки времени выполнения (или позже).
  
- [`libgdiplus`](https://github.com/mono/libgdiplus): реализация GDI API с открытым исходным кодом.

- Зависимости от .NET Core Runtime. Установка .NET Core Runtime сама по себе НЕ требуется.

- Для Python 3,5-3,7: необходима сборка `pymalloc` из Python. Опция сборки `--with-pymalloc` Python включена по умолчанию. Как правило, сборка `pymalloc` из Python помечена суффиксом `m` в имени файла.

- `libpython` поделились библиотекой Python. Опция сборки `--enable-shared` Python по умолчанию отключена, некоторые дистрибутивы Python не содержат общую библиотеку `libpython`. Для некоторых платформ Linux общая библиотека `libpython` может быть установлена с помощью менеджера пакетов, например: `sudo apt-get install libpython3.7`. Общая проблема заключается в том, что библиотека `libpython` установлена в другом месте, чем стандартная системная папка для общих библиотек. Проблема может быть исправлена с помощью параметров сборки Python для установки альтернативных путей к библиотеке при компиляции Python или путем создания символической ссылки на файл библиотеки `libpython` в стандартном расположении системы для общих библиотек. Обычно имя файла общей библиотеки `libpython` равно `libpythonX.Ym.so.1.0` для Python 3,5-3,7 или `libpythonX.Y.so.1.0` для Python 3,8 или более поздней версии (например: libpython3.7m.so.1.0, libpython3.9.so. 1,0).



Кроме того, любая операционная система, которая может установить Mono(поддержка .NET 4,0 Framework) или использовать ядро .NET, может использовать Aspose.3D for Python via .NET.
##  **Рендеринг**
###  **Вулкан**
Aspose.3D for Python via .NET требует платформы Vulkan x64, x86 не поддерживается.

- AMD Radeon 7700 серии и новее
- Серия NVIDIA GeForce 600 и новее
- Intel Skylake и новее
