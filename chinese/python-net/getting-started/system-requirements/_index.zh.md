---
title: 系统要求
type: docs
weight: 50
url: /zh/python-net/system-requirements/
description: 系统对Python via .NET Aspose.3D的要求。
---
## **概述**
` `要构建和操作3D文档格式，运行Aspose.3D Python via .NET的计算机不需要安装建模和渲染软件。Python via .NET Aspose.3D API还包含文档生成引擎。
## **支持的操作系统**
Aspose.3D for Python via .NET支持安装Python 3.5或更高版本的任何64位或32位操作系统。

<table>  
    <tr>
        <td style="font-weight: bold; width:400px">操作系统</td>
        <td style="font-weight: bold; width:400px">版本</td>
    </tr>
    <tr>
        <td>Microsoft Windows</td>
        <td>
            <ul>
                <li>Windows 2003服务器 (x64，x86)</li>
                <li>Windows 2008服务器 (x64，x86)</li>
                <li>Windows 2012服务器 (x64，x86)</li>
                <li>Windows 2012 R2服务器 (x64，x86)</li>
                <li>Windows 2016服务器 (x64，x86)</li>
                <li>Windows 2019服务器 (x64，x86)</li>
                <li>Windows XP (x64，x86)</li>
                <li>Windows Vista (x64，x86)</li>
                <li>Windows 7 (x64，x86)</li>
                <li>Windows 8，8.1 (x64，x86)</li>
                <li>Windows 10 (x64，x86)</li>
            </ul>
        </td>
    </tr>
    <tr>
        <td>Linux</td>
        <td>
            <ul>
                <li>乌班图</li>
                <li>OpenSUSE</li>
                <li>CentOS</li>
                <li>和其他人</li>
            </ul>
        </td>
    </tr>
</table>


## 目标Linux平台的系统要求

- GCC-6运行时库 (或更高版本)。
  
- [`libgdiplus`](https://github.com/mono/libgdiplus): GDI API的开源实现。

- .NET核心运行时的依赖关系。不需要安装.NET核心运行时本身。

- 对于Python 3.5-3.7: 需要`pymalloc`的Python构建。默认情况下启用`--with-pymalloc` Python生成选项。通常，Python的`pymalloc`构建在文件名中使用`m`后缀标记。

- `libpython`共享Python库。默认情况下，禁用`--enable-shared` Python生成选项，某些Python发行版不包含`libpython`的共享库。对于某些linux平台，可以使用包管理器安装`libpython`共享库，例如: `sudo apt-get install libpython3.7`。常见的问题是`libpython`库安装在与共享库的标准系统位置不同的位置。该问题可以通过在编译Python时使用Python构建选项来设置备用库路径来解决，或者通过在共享库的系统标准位置创建到`libpython`库文件的符号链接来解决。通常，`libpython`共享库文件名`libpythonX.Ym.so.1.0`用于Python 3.5-3.7，或`libpythonX.Y.so.1.0`用于Python 3.8或更高版本 (例如: libpython3.7m.so.1.0，libpython3.9.so.1.0)。



此外，任何可以安装Mono(.NET 4.0框架支持) 或使用.NET核心的操作系统都可以使用Aspose.3D进行Python via .NET。
## **渲染**
### **Vulkan**
Aspose.3D Python via .NET需要Vulkan x64平台，不支持x86。

- AMD Radeon 7700系列及更新
- NVIDIA GeForce 600系列及更新
- 英特尔Skylake和更新
