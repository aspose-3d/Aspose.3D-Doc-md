---
title: Ange 3D Filspararalternativ
type: docs
weight: 40
url: /sv/python-net/specify-3d-file-save-options/
description: Det finns flera Scene.Spara metod överbelastningar som accepterar ett SaveOptions objekt. Varje format spara har en motsvarande klass som innehar spara alternativ för det spara formatet.
---
##  **3D Filspararalternativ**
Det finns flera överbelastningar av [`Scene.save`](https://reference.aspose.com/3d/net/aspose.threed/scene) som accepterar ett `SaveOptions`-objekt. Detta bör vara ett föremål för en klass som härrör från klassen `SaveOptions`. Varje format spara har en motsvarande klass som innehåller spara alternativ för det spara formatet, till exempel, det finns `ColladaSaveOptions` för `FileFormat.Collada` spara formatet.
###  **Användning av Collada Spara inställningarna**
Koden nedan visar hur man ställer in sparalternativ innan en 3D-fil sparas till Collada-format.

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
###  **Användning av Discreet3DS Spara inställningarna**
Koden nedan visar hur man ställer in sparalternativ innan en 3D fil sparas till ett Discreet 3DS-format.

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
###  **Användning av FBX Spara inställningarna**
Koden nedan visar hur sparalternativ ska ställas innan en 3D-fil sparas till ett FBX-format.

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

`FBXSaveOptions` exponerar också `enable_compression` egenskap som kan användas för att komprimera större binärdata i FBX-filen. Standardvärdet för den här egenskapen är sant. Nedan förklarar kod snippet hur du kan arbeta med denna egendom medan du sparar en scen.



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
###  **Användning av Obj Spara alternativen**
Koden nedan visar hur sparalternativ ska anges innan en 3D fil sparas till ett Obj-format.

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
###  **Användning av STL Spara inställningarna**
Koden nedan visar hur man ställer in sparalternativ innan en 3D-fil sparas till STL-format.

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
###  **Användning av U3D Spara inställningarna**
Koden nedan visar hur sparalternativ ska anges innan ett dokument sparas till U3D format.

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
###  **Användning av glTF Spara inställningarna**
{{% alert color="primary" %}} 

Denna funktion stöds av version 19.8 eller större.

{{% /alert %}} 



Koden nedan visar hur sparalternativ ska anges innan ett dokument sparas till glTF format.

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
###  **PrettyPrint i glTF Spara inställningar**
Du kan också använda PrettyPrint-egenskapen för GLTFSaveOptions klass för människans förståelig JSON-utskrift. Koden nedan visar hur denna funktionalitet används.

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
###  **Spara beroenden för en 3D i det verkliga filsystemet**
Utvecklare kan behöva spara alla 3D-scener i det riktiga filsystemet. De kan definiera sökvägen för en lokal katalog, spara i MemoryFileSystem-objektet eller helt enkelt förkasta beroenden. Egenskapen FileSystem läggs till i alla spara alternativklasser.
####  **Kasta sparande av materialfiler**
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
####  **Spara beroende i lokalkatalog**
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
####  **Spara beroende i MemoryFileSystem- objekt**
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
###  **Användning av Google Draco (.drc) Spara inställningar**
Koden nedan visar hur sparalternativ ska ställas innan en 3D-modell sparas till DRC-formatet.

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
###  **Användning av RVM Spara inställningarna**
Koden nedan visar hur sparalternativ ska ställas innan en 3D-modell sparas till RVM-formatet.

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
