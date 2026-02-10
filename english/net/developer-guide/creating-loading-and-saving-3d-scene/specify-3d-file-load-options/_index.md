---
title: Specify 3D File Load Options in C#
linktitle: Specify 3D File Load Options
type: docs
weight: 30
url: /net/specify-3d-file-load-options/
description: There are several Scene.Open method overloads or Scene class constructor overloads that accept a LoadOptions object. Each load format has a corresponding class that holds load options for that load format.
---

## **Overview**

This article explains how you can load different types of 3D files using their respective load option classes in C# inside the Scene object and then you can [save it in different 3D supported file formats](https://docs.aspose.com/3d/net/specify-3d-file-save-options/). By loading and saving, you can perform number of different conversions e.g.

- Convert FBX to OBJ in C#
- Convert 3DS to FBX in C#
- Convert U3D to OBJ in C#
- Convert OBJ to 3DS in C#
- Convert X to 3DS in C#

## **3D File Load Options**
There are several [`Scene.Open`](https://reference.aspose.com/3d/net/aspose.threed/scene) method overloads or Scene class constructor overloads that accept a `LoadOptions` object. This should be an object of a class derived from the `LoadOptions` class. Each load format has a corresponding class that holds load options for that load format, for example there is `ColladaSaveOptions` for the `FileFormat.Collada` save format.
### **Use of the Discreet 3DS Load Options**
The C# code below shows how to set load options before loading a Discreet 3DS file.

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
### **Use of the Obj Load Options**
The C# code below shows how to set load options before loading an 3D Obj file.

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
### **Use of the STL Load Options**
The C# code below shows how to set load options before loading an STL file.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize an object
StlLoadOptions loadSTLOpts = new StlLoadOptions();
// Flip the coordinate system.
loadSTLOpts.FlipCoordinateSystem = true;
// Configure the look up paths to allow importer to find external dependencies.
loadSTLOpts.LookupPaths = new List<string>(new string[] { "textures" });

{{< /highlight >}}
### **Use of the U3D Load Options**
The C# code below shows how to set load options before loading a U3D file.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Initialize an object
U3dLoadOptions loadU3DOpts = new U3dLoadOptions();
// Flip the coordinate system.
loadU3DOpts.FlipCoordinateSystem = true;
// Configure the look up paths to allow importer to find external dependencies.
loadU3DOpts.LookupPaths = new List<string>(new string[] { "textures" });

{{< /highlight >}}
### **Use of the glTF Load Options**
The C# code below shows how to set load options before loading a glTF file.
#### **Flip the V/T Texture Coordinate**
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
### **Use of the Ply Load Options**
The C# code below shows how to set load options before loading a PLY model.

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
### **Use of the DirectX X Load Options**
The C# code below shows how to set load options before loading a DirectX X file.

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
### **Use RVM load options**
**C#**

{{< highlight java >}}

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
### **Using FBX Load Options**
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
