---
title: Especificar las opciones de carga de archivos 3D en C#
linktitle: Especificar 3D Opciones de carga de archivos
type: docs
weight: 30
url: /es/net/specify-3d-file-load-options/
description: Hay varias sobrecargas del método Scene.Open o sobrecargas del constructor de clases Scene que aceptan un objeto LoadOptions. Cada formato de carga tiene una clase correspondiente que contiene opciones de carga para ese formato de carga.
---
##  **Descripción general**

Este artículo explica cómo puede cargar diferentes tipos de archivos 3D utilizando sus respectivas clases de opción de carga en C# dentro del objeto Scene y luego puede [Guardarlo en diferentes formatos de archivo 3D compatibles](https://docs.aspose.com/3d/net/specify-3d-file-save-options/). Al cargar y guardar, puede realizar varias conversiones diferentes, p.

- Convierte FBX a OBJ en C#
- Convierte 3DS a FBX en C#
- Convierte U3D a OBJ en C#
- Convierte OBJ a 3DS en C#
- Convertir X a 3DS en C#

##  **3D Opciones de carga de archivos**
Hay varias sobrecargas de método [`Scene.Open`](https://reference.aspose.com/3d/net/aspose.threed/scene) o sobrecargas de constructor de clase Scene que aceptan un objeto `LoadOptions`. Este debe ser un objeto de una clase derivada de la clase `LoadOptions`. Cada formato de carga tiene una clase correspondiente que contiene opciones de carga para ese formato de carga, por ejemplo, hay `ColladaSaveOptions` para el formato de guardado `FileFormat.Collada`.
###  **Uso de las opciones de carga discreto 3DS**
El código C# a continuación muestra cómo establecer las opciones de carga antes de cargar un archivo Discreet 3DS.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
Discreet3dsLoadOptions loadOpts = new Discreet3dsLoadOptions();
// Sets wheather to use the transformation defined in the first frame of animation track.
loadOpts.ApplyAnimationTransform = true;
// Flip the coordinate system
loadOpts.FlipCoordinateSystem = true;
// Prefer to use gamma-corrected color if a 3ds file provides both original color and gamma-corrected color.
loadOpts.GammaCorrectedColor = true;
// Configure the look up paths to allow importer to find external dependencies.
loadOpts.LookupPaths = new List<string>(new string[] { "textures" });

{{< /highlight >}}
###  **Uso de las opciones de carga Obj**
El siguiente código C# muestra cómo establecer las opciones de carga antes de cargar un archivo 3D Obj.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize an object
ObjLoadOptions loadObjOpts = new ObjLoadOptions();
// Import materials from external material library file
loadObjOpts.EnableMaterials = true;
// Flip the coordinate system.
loadObjOpts.FlipCoordinateSystem = true;
// Configure the look up paths to allow importer to find external dependencies.
loadObjOpts.LookupPaths.Add("textures");

{{< /highlight >}}
###  **Uso de las opciones de carga STL**
El siguiente código C# muestra cómo establecer las opciones de carga antes de cargar un archivo STL.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize an object
StlLoadOptions loadSTLOpts = new StlLoadOptions();
// Flip the coordinate system.
loadSTLOpts.FlipCoordinateSystem = true;
// Configure the look up paths to allow importer to find external dependencies.
loadSTLOpts.LookupPaths = new List<string>(new string[] { "textures" });

{{< /highlight >}}
###  **Uso de las opciones de carga U3D**
El siguiente código C# muestra cómo establecer las opciones de carga antes de cargar un archivo U3D.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize an object
U3dLoadOptions loadU3DOpts = new U3dLoadOptions();
// Flip the coordinate system.
loadU3DOpts.FlipCoordinateSystem = true;
// Configure the look up paths to allow importer to find external dependencies.
loadU3DOpts.LookupPaths = new List<string>(new string[] { "textures" });

{{< /highlight >}}
###  **Uso de las opciones de carga glTF**
El siguiente código C# muestra cómo establecer las opciones de carga antes de cargar un archivo glTF.
####  **Voltear la coordenadas de textura V/T**
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize Scene class object
Scene scene = new Scene();
// Set load options
GltfLoadOptions loadOpt = new GltfLoadOptions();
// The default value is true, usually we don't need to change it. Aspose.3D will automatically flip the V/T texture coordinate during load and save.       
loadOpt.FlipTexCoordV = true;
scene.Open("Duck.gltf", loadOpt);

{{< /highlight >}}
###  **Uso de las opciones de carga de nivel**
El siguiente código C# muestra cómo establecer las opciones de carga antes de cargar un modelo PLY.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// initialize Scene class object
Scene scene = new Scene();
// initialize an object
PlyLoadOptions loadPLYOpts = new PlyLoadOptions();
// Flip the coordinate system.
loadPLYOpts.FlipCoordinateSystem = true;
// load 3D Ply model
scene.Open("vase-v2.ply", loadPLYOpts);

{{< /highlight >}}
###  **Uso de las opciones de carga de DirectX X**
El siguiente código C# muestra cómo establecer las opciones de carga antes de cargar un archivo DirectX X.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// initialize Scene class object
Scene scene = new Scene();
// initialize an object
XLoadOptions loadXOpts = new XLoadOptions(FileContentType.ASCII);
// flip the coordinate system.
loadXOpts.FlipCoordinateSystem = true;
// load 3D X file
scene.Open("warrior.x", loadXOpts);

{{< /highlight >}}
###  **Usar opciones de carga RVM**
**C#**

{{< highlight "java" >}}

 // set load options of RVM

Scene scene = new Scene();

var opt = new RvmLoadOptions()

{

    CylinderRadialSegments = 32,

    DishLatitudeSegments = 16,

    DishLongitudeSegments = 24,

    TorusTubularSegments = 40

};

// import RVM

scene.Open("LAD-TOP.rvm", opt);

// save in the OBJ format

scene.Save("LAD-TOP.obj", FileFormat.WavefrontOBJ);

{{< /highlight >}}
###  **Uso de las opciones de carga FBX**
{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
//This will output all properties defined in GlobalSettings in FBX file.
Scene scene = new Scene();
var opt = new FbxLoadOptions() { KeepBuiltinGlobalSettings = true };
scene.Open("test.FBX", opt);
foreach (Property property in scene.RootNode.AssetInfo.Properties)
{
    Console.WriteLine(property);
}

{{< /highlight >}}
