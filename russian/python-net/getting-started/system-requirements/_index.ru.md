---
title: Системные Требования
type: docs
weight: 50
url: /ru/python-net/system-requirements/
description: Системные требования для Aspose.3D для Python via .NET.
---
## **Обзор**
` `Для создания и управления форматами документов 3D машина, на которой работает Aspose.3D для Python via .NET, не нуждается в установленном программном обеспечении для моделирования и рендеринга. Aspose.3D для Python via .NET API также включает в себя механизм генерации документов.
## **Поддерживаемая операционная система**
Aspose.3D для Python via .NET поддерживает любую 64-разрядную или 32-разрядную операционную систему, в которой установлен Python 3,5 или более поздняя версия.

<table>  
    <tr>
        <td style="font-weight: bold; width:400px">Операционная система</td>
        <td style="font-weight: bold; width:400px">Версии</td>
    </tr>
    <tr>
        <td>Microsoft Windows</td>
        <td>
            <ul>
                <li>Сервер Windows 2003 (x64, x86)</li>
                <li>Сервер Windows 2008 (x64, x86)</li>
                <li>Сервер Windows 2012 (x64, x86)</li>
                <li>Сервер Windows 2012 R2 (x64, x86)</li>
                <li>Windows 2016 Сервер (x64, x86)</li>
                <li>Windows 2019 Сервер (x64, x86)</li>
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
                <li>OpenSUSE</li>
                <li>ЦентОС</li>
                <li>И другие</li>
            </ul>
        </td>
    </tr>
</table>


## Требования к системе для Target Linux Platform

- GCC-6 библиотеки времени выполнения (или позже).
  
- [`libgdiplus`](https://github.com/mono/libgdiplus): реализация с открытым исходным кодом GDI API.

- Зависимости от основной среды выполнения .NET. Сама установка .NET Core Runtime НЕ требуется.

- Для Python 3,5-3,7: необходима сборка `pymalloc` Python. Опция сборки `--with-pymalloc` Python включена по умолчанию. Обычно сборка `pymalloc` Python помечена суффиксом `m` в имени файла.

- `libpython` поделился библиотекой Python. Опция сборки `--enable-shared` Python по умолчанию отключена, некоторые дистрибутивы Python не содержат общую библиотеку `libpython`. Для некоторых платформ Linux с помощью диспетчера пакетов можно установить общую библиотеку `libpython`, например: `sudo apt-get install libpython3.7`. Общая проблема заключается в том, что библиотека `libpython` установлена в другом месте, чем стандартное системное местоположение для общих библиотек. Проблема может быть устранена с помощью параметров сборки Python для установки альтернативных путей к библиотеке при компиляции Python или исправлена путем создания символической ссылки на файл библиотеки `libpython` в стандартном местоположении системы для общих библиотек. Как правило, имя файла общей библиотеки `libpython`-`libpythonX.Ym.so.1.0` для Python 3,5-3,7 или `libpythonX.Y.so.1.0` для Python 3,8 или более поздней версии (например: libpython3.7m.so.1.0, libpython3.9.so). 1,0).



Кроме того, любая операционная система, которая может установить Mono (поддержка .NET 4,0 Framework) или использовать ядро .NET, может использовать Aspose.3D для Python via .NET.
## **Рендеринг**
### **Вулкан**
Aspose.3D для Python via .NET требуется платформа Vulkan x64, x86 не поддерживается.

- AMD Radeon 7700 серии и новее
- Серия NVIDIA GeForce 600 и новее
- Intel Skylake и новее
