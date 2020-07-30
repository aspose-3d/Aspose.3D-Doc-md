---
title : "Specify 3D File Save Options" 
description : "" 
weight : 16017 
toc : false
type: docs
url: /java/developerguide/cr-ld-sv/sv3ddoc/specify+3d+file+save+options/
---

# Aspose.3D for Java : Specify 3D File Save Options


{{< panel title="Contents Summary" style="primary" >}}
*   1 [3D File Save Options](#3d-file-save-options)
    *   1.1 [Use of Collada Save Options](#use-of-collada-save-options)
    *   1.2 [Use of Discreet3DS Save Options](#use-of-discreet3ds-save-options)
    *   1.3 [Use of the FBX Save Options](#use-of-the-fbx-save-options)
    *   1.4 [Use of OBJ Save Options](#use-of-obj-save-options)
    *   1.5 [Use of STL Save Options](#use-of-stl-save-options)
    *   1.6 [Use of the U3D Save Options](#use-of-the-u3d-save-options)
    *   1.7 [Use of the glTF Save Options](#use-of-the-gltf-save-options)
    *   1.8 [PrettyPrint in glTF Save Options](#prettyprint-in-gltf-save-options)
    *   1.9 [Save Dependencies of a 3D Scene in the Real File System](#save-dependencies-of-a-3d-scene-in-the-real-file-system)
        *   1.9.1 [Discard Saving the Material Files](#discard-saving-the-material-files)
        *   1.9.2 [Save Dependencies in the Local Directory](#save-dependencies-in-the-local-directory)
        *   1.9.3 [Save Dependencies in the MemoryFileSystem Instance](#save-dependencies-in-the-memoryfilesystem-instance)
    *   1.10 [Use of the Google Draco (.DRC) Save Options](#use-of-the-google-draco-(.drc)-save-options)SaveOptions)
    *   1.11 [Use of RVM Save Options](#use-of-rvm-save-options)
{{< /panel >}}
 

 

## 3D File Save Options

There are several `Scene.save` method overloads that accept a `SaveOptions` instance. This should be an instance of a class derived from the `SaveOptions` class. Each save format has a corresponding class that holds save options for that save format, for example there is `ColladaSaveOptions` for the `FileFormat.COLLADA` save format.

### Use of Collada Save Options

The code below shows how to set save options before saving a 3D file in Collada format.

### Use of Discreet3DS Save Options

The code below shows how to set save options before saving a 3D file to a Discreet 3DS format.

### Use of the FBX Save Options

The code below shows how to set save options before saving a 3D file to an FBX format.

### Use of OBJ Save Options

The code below shows how to set save options before saving a 3D file to an Obj format.

### Use of STL Save Options

The code below shows how to set save options before saving a 3D file to STL format.

### Use of the U3D Save Options

The code below shows how to set save options before saving a document to U3D format.

### Use of the glTF Save Options

This feature is supported by version 19.8 or greater.

The code below shows how to set save options before saving a document to glTF format.

### PrettyPrint in glTF Save Options

You can also use setPrettyPrint method of GLTFSaveOptions class for human-understandable JSON print. The code below shows how to use this functionality. 

### Save Dependencies of a 3D Scene in the Real File System

Developers may require to save all dependencies of 3D scene in the real file system. They can define the path of a local directory, save in the MemoryFileSystem object or simply discard dependencies. The `FileSystem` property is added in the all save option classes.

#### Discard Saving the Material Files

#### Save Dependencies in the Local Directory

#### Save Dependencies in the MemoryFileSystem Instance

### Use of the Google Draco (.DRC) Save Options

The code below shows how to set save options before saving a 3D model to DRC format.

### Use of RVM Save Options

The code below shows how to set save options before saving a 3D model to RVM format.

