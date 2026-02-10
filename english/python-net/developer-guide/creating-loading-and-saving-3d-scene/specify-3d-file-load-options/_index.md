---
title: Specify 3D File Load Options
type: docs
weight: 30
url: /python-net/specify-3d-file-load-options/
description: There are several Scene.Open method overloads or Scene class constructor overloads that accept a LoadOptions object. Each load format has a corresponding class that holds load options for that load format.
---

## **3D File Load Options**
There are several [`Scene.open`](https://reference.aspose.com/3d/net/aspose.threed/scene) method overloads or Scene class constructor overloads that accept a `LoadOptions` object. This should be an object of a class derived from the `LoadOptions` class. Each load format has a corresponding class that holds load options for that load format, for example there is `ColladaSaveOptions` for the `FileFormat.Collada` save format.
### **Use of the Discreet 3DS Load Options**
The code below shows how to set load options before loading a Discreet 3DS file.

{{< highlight "python" >}}
from aspose.threed.formats import Discreet3dsLoadOptions

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  The path to the documents directory.
dataDir = "data-dir"
loadOpts = Discreet3dsLoadOptions()
#  Sets whether to use transformation defined in the first frame of the animation track.
loadOpts.apply_animation_transform = True
#  Flip the coordinate system
loadOpts.flip_coordinate_system = True
#  Prefer to use gamma-corrected color if a 3ds file provides both original color and gamma-corrected color.
loadOpts.gamma_corrected_color = True
#  Configure look up paths to allow importer to find external dependencies.
loadOpts.lookup_paths = [[dataDir]]
{{< /highlight >}}
### **Use of the Obj Load Options**
The code below shows how to set load options before loading an 3D Obj file.

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
### **Use of the STL Load Options**
The code below shows how to set load options before loading a STL file.

{{< highlight "python" >}}
from aspose.threed.formats import StlLoadOptions

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  The path to the documents directory.
dataDir = "data-dir"
#  Initialize an object
loadSTLOpts = StlLoadOptions()
#  Flip to coordinate system.
loadSTLOpts.flip_coordinate_system = True
#  Configure look up paths to allow importer to find external dependencies.
loadSTLOpts.lookup_paths = [[dataDir]]
{{< /highlight >}}
### **Use of the U3D Load Options**
The code below shows how to set load options before loading a U3D file.

{{< highlight "python" >}}
from aspose.threed.formats import U3dLoadOptions

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  The path to the documents directory.
dataDir = "data-dir"
#  Initialize an object
loadU3DOpts = U3dLoadOptions()
#  Flip to coordinate system.
loadU3DOpts.flip_coordinate_system = True
#  Configure look up paths to allow importer to find external dependencies.
loadU3DOpts.lookup_paths = [[dataDir]]
{{< /highlight >}}
### **Use of the glTF Load Options**
The code below shows how to set load options before loading a glTF file.
#### **Flip to V/T Texture Coordinate**
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
#  The default value is true, usually we don't need to change it. Aspose.3D will automatically flip to V/T texture coordinate during load and save.
loadOpt.flip_tex_coord_v = True
scene.open(dataDir + "Duck.gltf", loadOpt)
{{< /highlight >}}
### **Use of the Ply Load Options**
The code below shows how to set load options before loading a PLY model.

{{< highlight "python" >}}
from aspose.threed import Scene
from aspose.threed.formats import PlyLoadOptions

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  path to the documents directory.
dataDir = "data-dir"
#  initialize Scene class object
scene = Scene()
#  initialize an object
loadPLYOpts = PlyLoadOptions()
#  Flip to coordinate system.
loadPLYOpts.flip_coordinate_system = True
#  load 3D Ply model
scene.open("data-dir"  + "vase-v2.ply", loadPLYOpts)
{{< /highlight >}}
### **Use of the DirectX X Load Options**
The code below shows how to set load options before loading a DirectX X file.

{{< highlight "python" >}}
from aspose.threed import FileContentType, Scene
from aspose.threed.formats import XLoadOptions

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  path to the documents directory.
dataDir = "data-dir"
#  initialize Scene class object
scene = Scene()
#  initialize an object
loadXOpts = XLoadOptions(FileContentType.ASCII)
#  flip to coordinate system.
loadXOpts.flip_coordinate_system = True
#  load 3D X file
scene.open("data-dir"  + "warrior.x", loadXOpts)
{{< /highlight >}}
### **Use RVM load options**
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

### **Using FBX Load Options**
{{< highlight "python" >}}
from aspose.threed import Scene
from aspose.threed.formats import FbxLoadOptions

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
dataDir = "data-dir"
#  This will output all properties defined in GlobalSettings in FBX file.
scene = Scene()
options = FbxLoadOptions()
options.keep_builtin_global_settings = true
opt = options
scene.open(dataDir + "test.FBX", opt)
for property in scene.root_node.asset_info.properties:
    print(property)
{{< /highlight >}}
