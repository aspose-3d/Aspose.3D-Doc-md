---
title: 指定 3D 文件加载选项
type: docs
weight: 30
url: /zh/python-net/specify-3d-file-load-options/
description: 有几个接受LoadOptions对象的Scene.Open方法重载或Scene类构造函数重载。每种加载格式都有一个相应的类，该类保存该加载格式的加载选项。
---
##  **3D 文件加载选项**
有几个接受 `LoadOptions` 对象的 [`Scene.open`](https://reference.aspose.com/3d/net/aspose.threed/scene) 方法重载或Scene类构造函数重载。这应该是从 `LoadOptions` 类派生的类的对象。每个加载格式都有一个对应的类，用于保存该加载格式的加载选项，例如，对于 `FileFormat.Collada` 保存格式，有 `ColladaSaveOptions`。
###  **使用Discreet 3DS 加载选项**
下面的代码显示了如何在加载一个谨慎的 3DS 文件之前设置加载选项。

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-Discreet3DSOption.py" >}}
###  **使用Obj加载选项**
下面的代码显示了如何在加载 3D Obj文件之前设置加载选项。

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-ObjLoadOption.py" >}}
###  **STL 加载选项的使用**
下面的代码显示了如何在加载 STL 文件之前设置加载选项。

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-STLLoadOption.py" >}}
###  **U3D 加载选项的使用**
下面的代码显示了如何在加载 U3D 文件之前设置加载选项。

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-U3DLoadOption.py" >}}
###  **glTF 加载选项的使用**
下面的代码显示了如何在加载 glTF 文件之前设置加载选项。
####  **翻转V/T纹理坐标**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-glTFLoadOptions.py" >}}
###  **使用层载荷选项**
下面的代码显示了如何在加载 PLY 模型之前设置加载选项。

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-PlyLoadOptions.py" >}}
###  **使用DirectX X加载选项**
下面的代码显示了如何在加载DirectX文件之前设置加载选项。

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-XLoadOptions.py" >}}
###  **使用 RVM 加载选项**
**C#**

```py


import aspose.threed as a3d
# set load options of RVM

scene = a3d.Scene()

opt = a3d.formats.RvmLoadOptions()
opt.cylinder_radial_segments = 32
opt.dish_latitude_segments = 16
opt.dish_longitude_segments = 24
opt.torus_tubular_segments = 40

# import RVM

scene.open("LAD-TOP.rvm", opt);

# save in the OBJ format

scene.save("LAD-TOP.obj", a3d.FileFormat.WAVEFRONT_OBJ);

```

###  **使用 FBX 加载选项**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-FBXLoadOptions.py" >}}
