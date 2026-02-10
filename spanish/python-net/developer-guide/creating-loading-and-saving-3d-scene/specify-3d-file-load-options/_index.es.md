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

{{< highlight "python" >}}
from aspose.threed.formats import Discreet3dsLoadOptions

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  The path to the documents directory.
dataDir = "data-dir"
loadOpts = Discreet3dsLoadOptions()
#  Sets wheather to use the transformation defined in the first frame of animation track.
loadOpts.apply_animation_transform = True
#  Flip the coordinate system
loadOpts.flip_coordinate_system = True
#  Prefer to use gamma-corrected color if a 3ds file provides both original color and gamma-corrected color.
loadOpts.gamma_corrected_color = True
#  Configure the look up paths to allow importer to find external dependencies.
loadOpts.lookup_paths = [[dataDir]]

{{< /highlight >}}
###  **Uso de las opciones de carga Obj**
El siguiente código muestra cómo establecer opciones de carga antes de cargar un archivo 3D Obj.

{{< highlight "python" >}}
from aspose.threed.formats import ObjLoadOptions

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  The path to the documents directory.
dataDir = "data-dir"
#  Initialize an object
loadObjOpts = ObjLoadOptions()
#  Import materials from external material library file
loadObjOpts.enable_materials = True
#  Flip the coordinate system.
loadObjOpts.flip_coordinate_system = True
#  Configure the look up paths to allow importer to find external dependencies.
loadObjOpts.lookup_paths.append(dataDir)

{{< /highlight >}}
###  **Uso de las opciones de carga STL**
El siguiente código muestra cómo configurar las opciones de carga antes de cargar un archivo STL.

{{< highlight "python" >}}
from aspose.threed.formats import StlLoadOptions

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  The path to the documents directory.
dataDir = "data-dir"
#  Initialize an object
loadSTLOpts = StlLoadOptions()
#  Flip the coordinate system.
loadSTLOpts.flip_coordinate_system = True
#  Configure the look up paths to allow importer to find external dependencies.
loadSTLOpts.lookup_paths = [[dataDir]]

{{< /highlight >}}
###  **Uso de las opciones de carga U3D**
El siguiente código muestra cómo establecer las opciones de carga antes de cargar un archivo U3D.

{{< highlight "python" >}}
from aspose.threed.formats import U3dLoadOptions

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  The path to the documents directory.
dataDir = "data-dir"
#  Initialize an object
loadU3DOpts = U3dLoadOptions()
#  Flip the coordinate system.
loadU3DOpts.flip_coordinate_system = True
#  Configure the look up paths to allow importer to find external dependencies.
loadU3DOpts.lookup_paths = [[dataDir]]

{{< /highlight >}}
###  **Uso de las opciones de carga glTF**
El siguiente código muestra cómo establecer las opciones de carga antes de cargar un archivo glTF.
####  **Voltear la coordenadas de textura V/T**
{{< highlight "python" >}}
from aspose.threed import Scene
from aspose.threed.formats import GltfLoadOptions

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  The path to the documents directory.
dataDir = "data-dir"
#  Initialize Scene class object
scene = Scene()
#  Set load options
loadOpt = GltfLoadOptions()
#  The default value is true, usually we don't need to change it. Aspose.3D will automatically flip the V/T texture coordinate during load and save.
loadOpt.flip_tex_coord_v = True
scene.open(dataDir + "Duck.gltf", loadOpt)

{{< /highlight >}}
###  **Uso de las opciones de carga de nivel**
El siguiente código muestra cómo establecer las opciones de carga antes de cargar un modelo PLY.

{{< highlight "python" >}}
from aspose.threed import Scene
from aspose.threed.formats import PlyLoadOptions

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  the path to the documents directory.
dataDir = "data-dir"
#  initialize Scene class object
scene = Scene()
#  initialize an object
loadPLYOpts = PlyLoadOptions()
#  Flip the coordinate system.
loadPLYOpts.flip_coordinate_system = True
#  load 3D Ply model
scene.open("data-dir"  + "vase-v2.ply", loadPLYOpts)

{{< /highlight >}}
###  **Uso de las opciones de carga de DirectX X**
El siguiente código muestra cómo establecer las opciones de carga antes de cargar un archivo DirectX X.

{{< highlight "python" >}}
from aspose.threed import FileContentType, Scene
from aspose.threed.formats import XLoadOptions

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  the path to the documents directory.
dataDir = "data-dir"
#  initialize Scene class object
scene = Scene()
#  initialize an object
loadXOpts = XLoadOptions(FileContentType.ASCII)
#  flip the coordinate system.
loadXOpts.flip_coordinate_system = True
#  load 3D X file
scene.open("data-dir"  + "warrior.x", loadXOpts)

{{< /highlight >}}
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
{{< highlight "python" >}}
from aspose.threed import Scene
from aspose.threed.formats import FbxLoadOptions

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
dataDir = "data-dir"
# This will output all properties defined in GlobalSettings in FBX file.
scene = Scene()
options = FbxLoadOptions()
options.keep_builtin_global_settings = true 
opt = options
scene.open(dataDir + "test.FBX", opt)
for property in scene.root_node.asset_info.properties:
    print(property)

{{< /highlight >}}
