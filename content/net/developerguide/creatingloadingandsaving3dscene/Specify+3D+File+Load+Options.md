+++
title = "Specify 3D File Load Options" 
description = "" 
weight = 12015 
+++

Aspose.3D for .NET : Specify 3D File Load Options  

# Aspose.3D for .NET : Specify 3D File Load Options


{{< panel title="Contents Summary" style="primary" >}}
*   1 [3D File Load Options](#Specify3DFileLoadOptions-3DFileLoadOptions)
    *   1.1 [Use of the Discreet 3DS Load Options](#Specify3DFileLoadOptions-UseoftheDiscreet3DSLoadOptions)
    *   1.2 [Use of the Obj Load Options](#Specify3DFileLoadOptions-UseoftheObjLoadOptions)
    *   1.3 [Use of the STL Load Options](#Specify3DFileLoadOptions-UseoftheSTLLoadOptions)
    *   1.4 [Use of the U3D Load Options](#Specify3DFileLoadOptions-UseoftheU3DLoadOptions)
    *   1.5 [Use of the glTF Load Options](#Specify3DFileLoadOptions-UseoftheglTFLoadOptions)
        *   1.5.1 [Flip the V/T Texture Coordinate](#Specify3DFileLoadOptions-FliptheV/TTextureCoordinate)
    *   1.6 [Use of the Ply Load Options](#Specify3DFileLoadOptions-UseofthePlyLoadOptions)
    *   1.7 [Use of the DirectX X Load Options](#Specify3DFileLoadOptions-UseoftheDirectXXLoadOptions)
    *   1.8 [Use RVM load options](#Specify3DFileLoadOptions-UseRVMloadoptions)
    *   1.9 [Using FBX Load Options](#Specify3DFileLoadOptions-UsingFBXLoadOptions)
{{< /panel >}}
 

 

## 3D File Load Options

There are several [`Scene.Open`](http://www.aspose.com/api/net/3d/aspose.threed/scene) method overloads or `Scene` class constructor overloads that accept a `LoadOptions` object. This should be an object of a class derived from the `LoadOptions` class. Each load format has a corresponding class that holds load options for that load format, for example there is `ColladaSaveOptions` for the `FileFormat.Collada` save format.

### Use of the Discreet 3DS Load Options

The code below shows how to set load options before loading a Discreet 3DS file.

### Use of the Obj Load Options

The code below shows how to set load options before loading an 3D Obj file.

### Use of the STL Load Options

The code below shows how to set load options before loading an STL file.

### Use of the U3D Load Options

The code below shows how to set load options before loading a U3D file.

### Use of the glTF Load Options

The code below shows how to set load options before loading a glTF file.

#### Flip the V/T Texture Coordinate

### Use of the Ply Load Options

The code below shows how to set load options before loading a PLY model.

### Use of the DirectX X Load Options

The code below shows how to set load options before loading a DirectX X file.

### Use RVM load options

**C#**

{{< code lang="c#" >}}
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
{{< /code >}}

### Using FBX Load Options

