---
title: Feature List
type: docs
weight: 30
url: /python-net/feature-list/
---

Aspose.3D Features


## **Supported Platforms**

The platforms Aspose.3D for Python via .NET can be used on Windows x64 or x86 and wide range of Linux distributions with Python 3.5 or later installed. There are additional requirements to the target Linux platform:
- GCC-6 runtime libraries (or later)
- Dependencies of .NET Core Runtime. Installing .NET Core Runtime itself is NOT required
- For Python 3.5-3.7: The pymalloc build of Python is needed. The --with-pymalloc Python build option is enabled by default. Typically, the pymalloc build of Python is marked with m suffix in the filename.
- libpython shared Python library. The --enable-shared Python build option is disabled by default, some Python distributions do not contain the libpython shared library. For some linux platforms, the libpython shared library can be installed using the package manager, for example: sudo apt-get install libpython3.7. The common issue is that libpython library is installed in a different location than the standard system location for shared libraries. The issue can be fixed by using the Python build options to set alternate library paths when compiling Python, or fixed by creating a symbolic link to the libpython library file in the system standard location for shared libraries. Typically, the libpython shared library file name is libpythonX.Ym.so.1.0 for Python 3.5-3.7, or libpythonX.Y.so.1.0 for Python 3.8 or later (for example: libpython3.7m.so.1.0, libpython3.9.so.1.0).
- libgdiplus 6.0.1 or later


## **Feature Matrix**

|**Features** |` `FBX |` `Collada |` `glTF |` `glTF 2.0 |` `U3D |` `PDF |` `STL |` `OBJ |` `PLY |` `3DS |` `ASE |` `X |` `3MF |` `RVM |` `Draco |
| :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- | :- |
|` `Lambert Material |<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>| |<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>| |<p>![todo:image_alt_text](accept.png)</p><p> </p>| |<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>| | | |
|` `Phong Material |<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>| |<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>| |<p>![todo:image_alt_text](accept.png)</p><p> </p>| | |<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>| | | |
|` `Shader-based Material |<p>![todo:image_alt_text](accept.png)</p><p> </p>| |<p>![todo:image_alt_text](accept.png)</p><p> </p>| | | | | | | | | | | | |
|` `PBR Material | | | |<p>![todo:image_alt_text](accept.png)</p><p> </p>| | | | | | | | | | | |
|` `PBR Specular Material | | | |<p>![todo:image_alt_text](accept.png)</p><p> </p>| | | | | | | | | | | |
|` `Diffuse texture |<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>| |<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>| |<p>![todo:image_alt_text](accept.png)</p><p> </p>| |<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>| | |
|` `Advanced texture |<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>| |<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>| |<p>![todo:image_alt_text](accept.png)</p><p> </p>| | | | | | | |
|` `Polygon meshes |<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>| | | | | |<p>![todo:image_alt_text](accept.png)</p><p> </p>| | | | | |<p>![todo:image_alt_text](accept.png)</p><p> </p>| |
|` `Triangle-based meshes |<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|
|` `Vertex elements |<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>| |<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>| | |<p>![todo:image_alt_text](accept.png)</p><p> </p>|
|` `NURBS geometries |<p>![todo:image_alt_text](accept.png)</p><p> </p>| | | | | | | | | | | | | | |
|` `Parameterized geometries | | | | | | | | | | | | | |<p>![todo:image_alt_text](accept.png)</p><p> </p>| |
|` `Local transformation |<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>| | | |<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>| |<p>![todo:image_alt_text](accept.png)</p><p> </p>| |
|` `Instancing |<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>| | | | | | | | | |
|` `Scene graph |<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>| | | |<p>![todo:image_alt_text](accept.png)</p><p> </p>| |<p>![todo:image_alt_text](accept.png)</p><p> </p>| |<p>![todo:image_alt_text](accept.png)</p><p> </p>| |
|` `Custom property |<p>![todo:image_alt_text](accept.png)</p><p> </p>| |<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>| | | | | | | | | | | |
|` `Skeleton |<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>| | | | | | | | | | | | | |
|` `Morph deformer |<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>| | | | | | | | | | | | | |
|` `Property animation |<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>| | | | | | | | | | | | | |
|` `Mesh Compression |<p>![todo:image_alt_text](accept.png)</p><p> </p>| | | |<p>![todo:image_alt_text](accept.png)</p><p> </p>|<p>![todo:image_alt_text](accept.png)</p><p> </p>| | | | | | |<p>![todo:image_alt_text](accept.png)</p><p> </p>| |<p>![todo:image_alt_text](accept.png)</p><p> </p>|

