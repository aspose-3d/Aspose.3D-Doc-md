---
title: Especificar 3D Opciones de carga de archivos
type: docs
weight: 30
url: /es/python-net/specify-3d-file-load-options/
description: Hay varias sobrecargas del método Scene.Open o sobrecargas del constructor de clases Scene que aceptan un objeto LoadOptions. Cada formato de carga tiene una clase correspondiente que contiene opciones de carga para ese formato de carga.
---
##  **3D Opciones de carga de archivos**
Hay varias sobrecargas de método [`Scene.open`](https://reference.aspose.com/3d/net/aspose.threed/scene) o sobrecargas de constructor de clase Scene que aceptan un objeto `LoadOptions`. Este debe ser un objeto de una clase derivada de la clase `LoadOptions`. Cada formato de carga tiene una clase correspondiente que contiene opciones de carga para ese formato de carga, por ejemplo, hay `ColladaSaveOptions` para el formato de guardado `FileFormat.Collada`.
###  **Uso de las opciones de carga discreto 3DS**
El siguiente código muestra cómo establecer las opciones de carga antes de cargar un archivo Discreet 3DS.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-Discreet3DSOption.py" >}}
###  **Uso de las opciones de carga Obj**
El siguiente código muestra cómo establecer opciones de carga antes de cargar un archivo 3D Obj.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-ObjLoadOption.py" >}}
###  **Uso de las opciones de carga STL**
El siguiente código muestra cómo configurar las opciones de carga antes de cargar un archivo STL.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-STLLoadOption.py" >}}
###  **Uso de las opciones de carga U3D**
El siguiente código muestra cómo establecer las opciones de carga antes de cargar un archivo U3D.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-U3DLoadOption.py" >}}
###  **Uso de las opciones de carga glTF**
El siguiente código muestra cómo establecer las opciones de carga antes de cargar un archivo glTF.
####  **Voltear la coordenadas de textura V/T**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-glTFLoadOptions.py" >}}
###  **Uso de las opciones de carga de nivel**
El siguiente código muestra cómo establecer las opciones de carga antes de cargar un modelo PLY.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-PlyLoadOptions.py" >}}
###  **Uso de las opciones de carga de DirectX X**
El siguiente código muestra cómo establecer las opciones de carga antes de cargar un archivo DirectX X.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-XLoadOptions.py" >}}
###  **Usar opciones de carga RVM**
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

###  **Uso de las opciones de carga FBX**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-FBXLoadOptions.py" >}}
