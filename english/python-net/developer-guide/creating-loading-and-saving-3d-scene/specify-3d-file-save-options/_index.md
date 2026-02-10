---
title: Specify 3D File Save Options
type: docs
weight: 40
url: /python-net/specify-3d-file-save-options/
description: There are several Scene.Save method overloads that accept a SaveOptions object. Each save format has a corresponding class that holds save options for that save format.
---

## **3D File Save Options**
There are several [`Scene.save`](https://reference.aspose.com/3d/net/aspose.threed/scene) method overloads that accept a `SaveOptions` object. This should be an object of a class derived from the `SaveOptions` class. Each save format has a corresponding class that holds save options for that save format, for example, there is `ColladaSaveOptions` for the `FileFormat.Collada` save format.
### **Use of the Collada Save Options**
The code below shows how to set save options before saving a 3D file to Collada format.

{{< highlight "python" >}}
from aspose.threed.formats import ColladaSaveOptions, ColladaTransformStyle

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
dataDir = "data-dir"
saveColladaopts = ColladaSaveOptions()
#  Generates indented XML document
saveColladaopts.indented = True
#  The style of node transformation
saveColladaopts.transform_style = ColladaTransformStyle.MATRIX
#  Configure lookup paths to allow importer to find external dependencies.
saveColladaopts.lookup_paths = [[dataDir]]
{{< /highlight >}}
### **Use of the Discreet3DS Save Options**
The code below shows how to set save options before saving a 3D file to a Discreet 3DS format.

{{< highlight "python" >}}
from aspose.threed.formats import Discreet3dsSaveOptions

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  The path to the documents directory.
dataDir = "data-dir"
#  Initialize an object
saveOpts = Discreet3dsSaveOptions()
#  The start base for generating new name for duplicated names.
saveOpts.duplicated_name_counter_base = 2
#  The format of duplicated counter.
saveOpts.duplicated_name_counter_format = "NameFormat"
#  The separator between object's name and duplicated counter.
saveOpts.duplicated_name_separator = "Separator"
#  Allows to export cameras
saveOpts.export_camera = True
#  Allows to export light
saveOpts.export_light = True
#  Flip to coordinate system
saveOpts.flip_coordinate_system = True
#  Prefer to use gamma-corrected color if a 3ds file provides both original color and gamma-corrected color.
saveOpts.gamma_corrected_color = True
#  Use high-precise color which each color channel will use 32bit float.
saveOpts.high_precise_color = True
#  Configure lookup paths to allow importer to find external dependencies.
saveOpts.lookup_paths = [[dataDir]]
#  Set to master scale
saveOpts.master_scale = 1.0
{{< /highlight >}}
### **Use of the FBX Save Options**
The code below shows how to set save options before saving a 3D file to an FBX format.

{{< highlight "python" >}}
from aspose.threed import FileFormat
from aspose.threed.formats import FbxSaveOptions

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  The path to the documents directory.
dataDir = "data-dir"
#  Initialize an object
saveOpts = FbxSaveOptions(FileFormat.FBX7500ASCII)
#  Generates legacy material properties.
saveOpts.export_legacy_material_properties = True
#  Fold repeated curve data using FBX's animation reference count
saveOpts.fold_repeated_curve_data = True
#  Always generates material mapping information for geometries if attached node contains materials.
saveOpts.generate_vertex_element_material = True
#  Configure lookup paths to allow importer to find external dependencies.
saveOpts.lookup_paths = [[dataDir]]
#  Generates a video object for texture.
saveOpts.video_for_texture = True
{{< /highlight >}}

`FBXSaveOptions` also exposes `enable_compression` property which can be used to compress large binary data in the FBX file. Default value of this property is true. Below code snippet explains how can you work with this property while saving a scene.



{{< highlight "python" >}}
from aspose.threed import FileFormat, Scene
from aspose.threed.formats import FbxSaveOptions

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Load a 3D document into Aspose.3D
scene = Scene("data-dir"  + "document.fbx")
options = FbxSaveOptions(FileFormat.FBX7500ASCII)
options.enable_compression = false 
scene.save("out"  + "UncompressedDocument.fbx", options)

{{< /highlight >}}
### **Use of the Obj Save Options**
The code below shows how to set save options before saving a 3D file to an Obj format.

{{< highlight "python" >}}
from aspose.threed.formats import ObjSaveOptions

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  The path to the documents directory.
dataDir = "data-dir"
#  Initialize an object
saveObjOpts = ObjSaveOptions()
#  Import materials from external material library file
saveObjOpts.enable_materials = True
#  Flip to coordinate system.
saveObjOpts.flip_coordinate_system = True
#  Configure lookup paths to allow importer to find external dependencies.
saveObjOpts.lookup_paths = [[dataDir]]
#  Serialize W component in model's vertex position
saveObjOpts.serialize_w = True
#  Generate comments for each section
saveObjOpts.verbose = True
{{< /highlight >}}
### **Use of the STL Save Options**
The code below shows how to set save options before saving a 3D file to STL format.

{{< highlight "python" >}}
from aspose.threed.formats import StlSaveOptions

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  The path to the documents directory.
dataDir = "data-dir"
#  Initialize an object
saveSTLOpts = StlSaveOptions()
#  Flip to coordinate system.
saveSTLOpts.flip_coordinate_system = True
#  Configure lookup paths to allow importer to find external dependencies.
saveSTLOpts.lookup_paths = [[dataDir]]
{{< /highlight >}}
### **Use of the U3D Save Options**
The code below shows how to set save options before saving a document to U3D format.

{{< highlight "python" >}}
from aspose.threed.formats import U3dSaveOptions

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
dataDir = "data-dir"
saveU3DOpts = U3dSaveOptions()
#  Flip to coordinate system.
saveU3DOpts.flip_coordinate_system = True
#  Configure lookup paths to allow importer to find external dependencies.
saveU3DOpts.lookup_paths = [[dataDir]]
{{< /highlight >}}
### **Use of the glTF Save Options**
{{% alert color="primary" %}} 

This feature is supported by version 19.8 or greater.

{{% /alert %}} 



The code below shows how to set save options before saving a document to glTF format.

{{< highlight "python" >}}
from aspose.threed import FileContentType, FileFormat, Scene
from aspose.threed.entities import Sphere
from aspose.threed.formats import GltfSaveOptions

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Initialize Scene object
scene = Scene()
#  Create a child node
scene.root_node.create_child_node("sphere", Sphere())
#  Set glTF saving options. The code example embeds all assets into the target file usually a glTF file comes with some dependencies, a bin file for model's vertex/indices, two .glsl files for vertex/fragment shaders
#  Use opt.EmbedAssets to tells the Aspose.3D API to export scene and embed the dependencies inside the target file.
opt = GltfSaveOptions(FileContentType.ASCII)
opt.embed_assets = True
#  Use KHR_materials_common extension to define the material, thus no GLSL files are generated.
opt.use_common_materials = True
#  Customize the name of the buffer file which defines model
opt.buffer_file = "mybuf.bin"
#  Save GlTF file
scene.save("out"  + "glTFSaveOptions_out.gltf", opt)
#  Save a binary glTF file using KHR_binary_glTF extension
scene.save("out"  + "glTFSaveOptions_out.glb", FileFormat.GLTF_BINARY)
#  Developers may use saving options to create a binary glTF file using KHR_binary_glTF extension
opts = GltfSaveOptions(FileContentType.BINARY)
scene.save("out"  + "Test_out.glb", opts)

{{< /highlight >}}
### **PrettyPrint in glTF Save Options**
You can also use PrettyPrint property of GLTFSaveOptions class for human-understandable JSON print. The code below shows how to use this functionality. 

{{< highlight "python" >}}
from aspose.threed import FileFormat, Scene
from aspose.threed.entities import Sphere
from aspose.threed.formats import GltfSaveOptions

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Initialize 3D scene
scene = Scene()
#  Create a child node
scene.root_node.create_child_node("sphere", Sphere())
#  Initialize GltfSaveOptions
opt = GltfSaveOptions(FileFormat.GLTF2)
#  The JSON content of GLTF file is indented for human reading, default value is false
opt.pretty_print = True
#  Save 3D Scene
scene.save("data-dir"  + "prettyPrintInGltfSaveOption.gltf", opt)
{{< /highlight >}}
### **Save Dependencies of a 3D Scene in the Real File System**
Developers may require to save all 3D scene dependencies in the real file system. They can define the path of a local directory, save in the MemoryFileSystem object or simply discard dependencies. The FileSystem property is added in the all save option classes.
#### **Discard Saving the Material Files**
{{< highlight "python" >}}
from aspose.threed import Scene
from aspose.threed.entities import Sphere
from aspose.threed.formats import ObjSaveOptions
from aspose.threed.shading import PhongMaterial
from aspose.threed.utilities import DummyFileSystem

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  The code example uses the DummyFileSystem, so the material files are not created.
#  Initialize Scene object
scene = Scene()
#  Create a child node
scene.root_node.create_child_node("sphere", Sphere()).material = PhongMaterial()
#  Set saving options
opt = ObjSaveOptions()
opt.file_system = DummyFileSystem()
#  Save 3D scene
scene.save("out"  + "DiscardSavingMaterial_out.obj", opt)

{{< /highlight >}}
#### **Save Dependencies in the Local Directory**
{{< highlight "python" >}}
from aspose.threed import Scene
from aspose.threed.entities import Sphere
from aspose.threed.formats import ObjSaveOptions
from aspose.threed.shading import PhongMaterial
from aspose.threed.utilities import LocalFileSystem

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  The code example uses the LocalFileSystem class to save dependencies to the local directory.
dataDir = "data-dir"
#  Initialize Scene object
scene = Scene()
#  Create a child node
scene.root_node.create_child_node("sphere", Sphere()).material = PhongMaterial()
#  Set saving options
opt = ObjSaveOptions()
opt.file_system = LocalFileSystem(dataDir)
#  Save 3D scene
scene.save("out"  + "SavingDependenciesInLocalDirectory_out.obj", opt)

{{< /highlight >}}
#### **Save Dependencies in the MemoryFileSystem Object**
{{< highlight "python" >}}
from aspose.threed import Scene
from aspose.threed.entities import Sphere
from aspose.threed.formats import ObjSaveOptions
from aspose.threed.shading import PhongMaterial
from aspose.threed.utilities import MemoryFileSystem

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  The code example uses the MemoryFileSystem to intercepts the dependencies writing.
#  Initialize Scene object
scene = Scene()
#  Create a child node
scene.root_node.create_child_node("sphere", Sphere()).material = PhongMaterial()
#  Set saving options
opt = ObjSaveOptions()
mfs = MemoryFileSystem()
opt.file_system = mfs
#  Save 3D scene
scene.save("out"  + "SavingDependenciesInMemoryFileSystem_out.obj", opt)
#  Get the test.mtl file content
mtl = mfs.get_file_content("SavingDependenciesInMemoryFileSystem_out.mtl")
with open("out"  + "Material.mtl", "wb") as f:
    f.write(mtl)

{{< /highlight >}}
### **Use of the Google Draco (.drc) Save Options**
The code below shows how to set save options before saving a 3D model to DRC format.

{{< highlight "python" >}}
from aspose.threed import Scene
from aspose.threed.entities import Sphere
from aspose.threed.formats import DracoCompressionLevel, DracoSaveOptions

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Initialize Scene object
scene = Scene()
#  Create a child node
scene.root_node.create_child_node("sphere", Sphere())
#  Initialize .DRC saving options.
opts = DracoSaveOptions()
#  Quantization bits for position
opts.position_bits = 14
#  Quantization bits for texture coordinate
opts.texture_coordinate_bits = 8
#  Quantization bits for vertex color
opts.color_bits = 10
#  Quantization bits for normal vectors
opts.normal_bits = 7
#  Set compression level
opts.compression_level = DracoCompressionLevel.OPTIMAL
#  Save Google Draco (.drc) file
scene.save("out"  + "DRCSaveOptions_out.drc", opts)

{{< /highlight >}}
### **Use of the RVM Save Options**
The code below shows how to set save options before saving a 3D model to RVM format.

{{< highlight "python" >}}
from aspose.threed import Scene
from aspose.threed.entities import Box
from aspose.threed.formats import RvmSaveOptions

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
dataDir = "data-dir"
scene = Scene()
node = scene.root_node.create_child_node("Box", Box())
node.set_property("rvm:Refno", "=3462123")
node.set_property("rvm:Description", "This is the description of the box")
options = RvmSaveOptions()
options.attribute_prefix = "rvm:"
options.export_attributes = true 
# The RVM attribute's prefix is rvm:, all properties that starts with rvm: will be exported to .att file(the prefix will be removed)
opt = options
scene.save(dataDir + "test.rvm", opt)

{{< /highlight >}}
