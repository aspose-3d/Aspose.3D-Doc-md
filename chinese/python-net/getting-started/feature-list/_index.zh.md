---
title: 特性列表
type: docs
weight: 30
url: /zh/python-net/feature-list/
---
Aspose.3D 功能


##  **支持的平台**

平台 Aspose.3D for Python via .NET 可用于 Windows x64或x86以及安装了 Python 3.5或更高版本的各种Linux发行版。目标Linux平台还有其他要求:
- GCC-6运行时库 (或更高版本)
- .NET 核心运行时的依赖项。不需要安装 .NET 核心运行时本身
- 对于 Python 3.5 3.7: 需要 Python 的pymalloc构建。默认情况下启用 -- 与-pymalloc Python 构建选项。通常，Python 的pymalloc版本在文件名中标记为m后缀。
- libpython共享 Python 库。默认情况下禁用 -- enable-shared Python 构建选项，某些 Python 发行版不包含libpython共享库。对于某些linux平台，可以使用包管理器安装libpython共享库，例如: sudo apt-get install libpython3.7。常见的问题是libpython库安装在与共享库的标准系统位置不同的位置。可以通过在编译 Python 时使用 Python 构建选项设置备用库路径来修复此问题，也可以通过在共享库的系统标准位置中创建指向libpython库文件的符号链接来修复此问题。通常，对于 Python 3.5 3.7，libpython共享库文件名为libpythonX.Ym.so.1.0; 对于 Python 3.8或更高版本，libpythonX.Y.so.1.0 (例如: libpython3.7m.so.1.0、libpython3.9.so.1.0)。
- libgdiplus 6.0.1或更高版本


##  **特性矩阵**

|**功能** |` `FBX|` `Collada|` `glTF|` `glTF 2.0|` `U3D|` `PDF|` `STL|` `OBJ|` `PLY|` `3DS|` `ASE|` `X|` `3MF|` `RVM|` `Draco|
| :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- |
|` `Lambert材料|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>| |<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>| |<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>| |<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>| | | |
|` `Phong材料|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>| |<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>| |<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>| | |<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>| | | |
|` ` 基于着色器的材质|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>| |<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>| | | | | | | | | | | | |
|` `PBR材料| | | |<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>| | | | | | | | | | | |
|` `PBR镜面材质| | | |<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>| | | | | | | | | | | |
|` ` 漫反射纹理|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>| |<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>| |<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>| |<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>| | |
|` ` 高级纹理|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>| |<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>| |<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>| | | | | | | |
|` ` 多边形网格|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>| | | | | |<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>| | | | | |<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>| |
|` ` 基于三角形的网格|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>|
|` ` 顶点元素|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>| |<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>| | |<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>|
|` `NURBS几何图形|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>| | | | | | | | | | | | | | |
|` ` 参数化几何图形| | | | | | | | | | | | | |<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>| |
|` ` 本地转换|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>| | | |<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>| |<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>| |
|` ` 实例化|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>| | | | | | | | | |
|` ` 场景图|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>| | | |<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>| |<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>| |<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>| |
|` ` 自定义属性|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>| |<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>| | | | | | | | | | | |
|` ` 骨架|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>| | | | | | | | | | | | | |
|` ` 变形变形器|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>| | | | | | | | | | | | | |
|` ` 属性动画|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>| | | | | | | | | | | | | |
|` ` 网格压缩|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>| | | |<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>|<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>| | | | | | |<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>| |<p>![todo: 图像 _ alt_text](accept.png)</p><p> </p>|

