---
title: Укажите параметры загрузки файла 3D
type: docs
weight: 30
url: /ru/python-net/specify-3d-file-load-options/
description: Существует несколько перегрузок метода Scene.Open или перегрузок конструктора класса Scene, которые принимают объект LoadOptions. Каждый формат нагрузки имеет соответствующий класс, который содержит параметры загрузки для этого формата нагрузки.
---
##  **3D Параметры загрузки файла**
Существует несколько перегрузок метода [`Scene.open`](https://reference.aspose.com/3d/net/aspose.threed/scene) или перегрузок конструктора класса Scene, которые принимают объект `LoadOptions`. Это должен быть объект класса, производного от класса `LoadOptions`. Каждый формат загрузки имеет соответствующий класс, который содержит параметры загрузки для этого формата загрузки, например, есть `ColladaSaveOptions` для формата сохранения `FileFormat.Collada`.
###  **Использование дискретных параметров загрузки 3DS**
Код ниже показывает, как установить параметры загрузки перед загрузкой файла Discreet 3DS.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-Discreet3DSOption.py" >}}
###  **Использование опций нагрузки Obj**
Код ниже показывает, как установить параметры загрузки перед загрузкой файла 3D Obj.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-ObjLoadOption.py" >}}
###  **Использование параметров загрузки STL**
Код ниже показывает, как установить параметры загрузки перед загрузкой файла STL.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-STLLoadOption.py" >}}
###  **Использование параметров загрузки U3D**
Код ниже показывает, как установить параметры загрузки перед загрузкой файла U3D.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-U3DLoadOption.py" >}}
###  **Использование параметров загрузки glTF**
Код ниже показывает, как установить параметры загрузки перед загрузкой файла glTF.
####  **Переверните координату текстуры V/T**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-glTFLoadOptions.py" >}}
###  **Использование опций нагрузки Ply**
Код ниже показывает, как установить параметры загрузки перед загрузкой модели PLY.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-PlyLoadOptions.py" >}}
###  **Использование опций нагрузки DirectX X**
Код ниже показывает, как установить параметры загрузки перед загрузкой файла DirectX X.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-XLoadOptions.py" >}}
###  **Используйте параметры загрузки RVM**
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

###  **Использование параметров загрузки FBX**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-FBXLoadOptions.py" >}}
