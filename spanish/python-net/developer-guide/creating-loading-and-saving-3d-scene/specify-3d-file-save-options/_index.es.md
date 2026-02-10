---
title: Especificar las opciones de guardado de archivos 3D
type: docs
weight: 40
url: /es/python-net/specify-3d-file-save-options/
description: Hay varias sobrecargas del método Scene.Save que aceptan un objeto SaveOptions. Cada formato de guardado tiene una clase correspondiente que contiene opciones de guardado para ese formato de guardado.
---
##  **3D Opciones para guardar archivos**
Existen varias sobrecargas de métodos [`Scene.save`](https://reference.aspose.com/3d/net/aspose.threed/scene) que aceptan un objeto `SaveOptions`. Este debe ser un objeto de una clase derivada de la clase `SaveOptions`. Cada formato de guardado tiene una clase correspondiente que contiene opciones de guardado para ese formato de guardado, por ejemplo, hay `ColladaSaveOptions` para el formato de guardado `FileFormat.Collada`.
###  **Uso de las opciones de guardado Collada**
El siguiente código muestra cómo establecer las opciones de guardado antes de guardar un archivo 3D en formato Collada.

{{< highlight "python" >}}
from aspose.threed.formats import ColladaSaveOptions, ColladaTransformStyle

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
dataDir = "data-dir"
saveColladaopts = ColladaSaveOptions()
#  Generates indented XML document
saveColladaopts.indented = True
#  The style of node transformation
saveColladaopts.transform_style = ColladaTransformStyle.MATRIX
#  Configure the lookup paths to allow importer to find external dependencies.
saveColladaopts.lookup_paths = [[dataDir]]

{{< /highlight >}}
###  **Uso de las opciones de guardado Discreet3DS**
El siguiente código muestra cómo configurar las opciones de guardado antes de guardar un archivo 3D en formato Discreet 3DS.

{{< highlight "python" >}}
from aspose.threed.formats import Discreet3dsSaveOptions

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  The path to the documents directory.
dataDir = "data-dir"
#  Initialize an object
saveOpts = Discreet3dsSaveOptions()
#  The start base for generating new name for duplicated names.
saveOpts.duplicated_name_counter_base = 2
#  The format of the duplicated counter.
saveOpts.duplicated_name_counter_format = "NameFormat"
#  The separator between object's name and the duplicated counter.
saveOpts.duplicated_name_separator = "Separator"
#  Allows to export cameras
saveOpts.export_camera = True
#  Allows to export light
saveOpts.export_light = True
#  Flip the coordinate system
saveOpts.flip_coordinate_system = True
#  Prefer to use gamma-corrected color if a 3ds file provides both original color and gamma-corrected color.
saveOpts.gamma_corrected_color = True
#  Use high-precise color which each color channel will use 32bit float.
saveOpts.high_precise_color = True
#  Configure the look up paths to allow importer to find external dependencies.
saveOpts.lookup_paths = [[dataDir]]
#  Set the master scale
saveOpts.master_scale = 1.0

{{< /highlight >}}
###  **Uso de las opciones de guardado FBX**
El siguiente código muestra cómo configurar las opciones de guardado antes de guardar un archivo 3D en un formato FBX.

{{< highlight "python" >}}
from aspose.threed import FileFormat
from aspose.threed.formats import FbxSaveOptions

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  The path to the documents directory.
dataDir = "data-dir"
#  Initialize an object
saveOpts = FbxSaveOptions(FileFormat.FBX7500ASCII)
#  Generates the legacy material properties.
saveOpts.export_legacy_material_properties = True
#  Fold repeated curve data using FBX's animation reference count
saveOpts.fold_repeated_curve_data = True
#  Always generates material mapping information for geometries if the attached node contains materials.
saveOpts.generate_vertex_element_material = True
#  Configure the look up paths to allow importer to find external dependencies.
saveOpts.lookup_paths = [[dataDir]]
#  Generates a video object for texture.
saveOpts.video_for_texture = True

{{< /highlight >}}

`FBXSaveOptions` también expone la propiedad `enable_compression` que se puede usar para comprimir datos binarios grandes en el archivo FBX. El valor predeterminado de esta propiedad es true. A continuación, el fragmento de código explica cómo puede trabajar con esta propiedad mientras guarda una escena.



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
###  **Uso de las opciones de Obj Save**
El siguiente código muestra cómo configurar las opciones de guardado antes de guardar un archivo 3D en un formato Obj.

{{< highlight "python" >}}
from aspose.threed.formats import ObjSaveOptions

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  The path to the documents directory.
dataDir = "data-dir"
#  Initialize an object
saveObjOpts = ObjSaveOptions()
#  Import materials from external material library file
saveObjOpts.enable_materials = True
#  Flip the coordinate system.
saveObjOpts.flip_coordinate_system = True
#  Configure the look up paths to allow importer to find external dependencies.
saveObjOpts.lookup_paths = [[dataDir]]
#  Serialize W component in model's vertex position
saveObjOpts.serialize_w = True
#  Generate comments for each section
saveObjOpts.verbose = True

{{< /highlight >}}
###  **Uso de las opciones de guardado STL**
El siguiente código muestra cómo establecer las opciones de guardado antes de guardar un archivo 3D en formato STL.

{{< highlight "python" >}}
from aspose.threed.formats import StlSaveOptions

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  The path to the documents directory.
dataDir = "data-dir"
#  Initialize an object
saveSTLOpts = StlSaveOptions()
#  Flip the coordinate system.
saveSTLOpts.flip_coordinate_system = True
#  Configure the look up paths to allow importer to find external dependencies.
saveSTLOpts.lookup_paths = [[dataDir]]

{{< /highlight >}}
###  **Uso de las opciones de guardado U3D**
El siguiente código muestra cómo configurar las opciones de guardado antes de guardar un documento en formato U3D.

{{< highlight "python" >}}
from aspose.threed.formats import U3dSaveOptions

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  The path to the documents directory.
dataDir = "data-dir"
#  Initialize an object
saveU3DOptions = U3dSaveOptions()
#  Export normal data.
saveU3DOptions.export_normals = True
#  Export the texture coordinates.
saveU3DOptions.export_texture_coordinates = True
#  Export the vertex diffuse color.
saveU3DOptions.export_vertex_diffuse = True
#  Export vertex specular color
saveU3DOptions.export_vertex_specular = True
#  Flip the coordinate system.
saveU3DOptions.flip_coordinate_system = True
#  Configure the look up paths to allow importer to find external dependencies.
saveU3DOptions.lookup_paths = [[dataDir]]
#  Compress the mesh data
saveU3DOptions.mesh_compression = True

{{< /highlight >}}
###  **Uso de las opciones de guardado glTF**
{{% alert color="primary" %}} 

Esta característica es compatible con la versión 19,8 o superior.

{{% /alert %}} 



El siguiente código muestra cómo configurar las opciones de guardado antes de guardar un documento en formato glTF.

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
###  **PrettyPrint en glTF Guardar opciones**
También puede utilizar la propiedad PrettyPrint de la clase GLTFSaveOptions para la impresión JSON comprensible para el ser humano. El siguiente código muestra cómo usar esta funcionalidad.

{{< highlight "python" >}}
from aspose.threed import FileFormat, Scene
from aspose.threed.entities import Sphere
from aspose.threed.formats import GltfSaveOptions

#  For complete examples and data files, please go to https:# github.com/aspose-3d/Aspose.3D-for-.NET
#  Initialize 3D scene
scene = Scene(Sphere())
#  Initialize GltfSaveOptions
opt = GltfSaveOptions(FileFormat.GLTF2)
#  The JSON content of GLTF file is indented for human reading, default value is false
opt.pretty_print = True
#  Save 3D Scene
scene.save("data-dir"  + "prettyPrintInGltfSaveOption.gltf", opt)

{{< /highlight >}}
###  **Guardar dependencias de una escena 3D en el sistema de archivos real**
Los desarrolladores pueden requerir guardar todas las dependencias de escena 3D en el sistema de archivos real. Pueden definir la ruta de un directorio local, guardar en el objeto MemoryFileSystem o simplemente descartar dependencias. La propiedad FileSystem se agrega en las clases de opción all save.
####  **Descarte guardar los archivos de material**
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
####  **Guardar dependencias en el directorio local**
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
####  **Guardar dependencias en el objeto MemoryFileSystem**
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
###  **Uso de las opciones de guardado Google Draco (.drc)**
El siguiente código muestra cómo configurar las opciones de guardado antes de guardar un modelo 3D en formato DRC.

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
###  **Uso de las opciones de guardado RVM**
El siguiente código muestra cómo configurar las opciones de guardado antes de guardar un modelo 3D en formato RVM.

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
