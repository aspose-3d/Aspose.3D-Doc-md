---
title : "Specify 3D File Load Options" 
description : "" 
weight : 16015 
toc : false
type: docs
url: /java/developerguide/cr-ld-sv/rd3ddoc/specify+3d+file+load+options/
---

# Aspose.3D for Java : Specify 3D File Load Options


{{< panel title="Contents Summary" style="primary" >}}
*   1 [3D File Load Options](#3d-file-load-options)
    *   1.1 [Use of the Discreet 3DS Load Options](#use-of-the-discreet-3ds-load-options)
    *   1.2 [Use of the Obj Load Options](#use-of-the-obj-load-options)
    *   1.3 [Use of the STL Load Options](#use-of-the-stl-load-options)
    *   1.4 [Use of the U3D Load Options](#use-of-the-u3d-load-options)
    *   1.5 [Use of the glTF Load Options](#use-of-the-gltf-load-options)
        *   1.5.1 [Flip the V/T Texture Coordinate](#flip-the-v/t-texture-coordinate)
    *   1.6 [Use of the Ply Load Options](#use-of-the-ply-load-options)
    *   1.7 [Use of the DirectX X Load Options](#use-of-the-directx-x-load-options)
    *   1.8 [Use FBX Load Options](#use-fbx-load-options)
{{< /panel >}}
 

 

## 3D File Load Options

There are several `Scene.open` method overloads or `Scene` class constructor overloads that accept `LoadOptions` instance. This should be an instance of a class derived from the `LoadOptions` class. Each load format has a corresponding class that holds load options for that load format, for example there is `ColladaSaveOptions` for the `FileFormat.COLLADA` save format.

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

### Use FBX Load Options

