+++
title = "Specify 3D File Save Options" 
description = "" 
weight = 12016 
+++

Aspose.3D for .NET : Specify 3D File Save Options  

# Aspose.3D for .NET : Specify 3D File Save Options


{{< panel title="Contents Summary" style="primary" >}}
*   1 [3D File Save Options](#Specify3DFileSaveOptions-3DFileSaveOptions)
    *   1.1 [Use of the Collada Save Options](#Specify3DFileSaveOptions-UseoftheColladaSaveOptions)
    *   1.2 [Use of the Discreet3DS Save Options](#Specify3DFileSaveOptions-UseoftheDiscreet3DSSaveOptions)
    *   1.3 [Use of the FBX Save Options](#Specify3DFileSaveOptions-UseoftheFBXSaveOptions)
    *   1.4[  
{{< /panel >}}
    *   1.5 [Use of the STL Save Options](#Specify3DFileSaveOptions-UseoftheSTLSaveOptions)
    *   1.6 [Use of the U3D Save Options](#Specify3DFileSaveOptions-UseoftheU3DSaveOptions)
    *   1.7 [Use of the glTF Save Options](#Specify3DFileSaveOptions-UseoftheglTFSaveOptions)
    *   1.8 [PrettyPrint in glTF Save Options](#Specify3DFileSaveOptions-PrettyPrintinglTFSaveOptions)
    *   1.9 [Save Dependencies of a 3D Scene in the Real File System](#Specify3DFileSaveOptions-SaveDependenciesofa3DSceneintheRealFileSystem)
        *   1.9.1 [Discard Saving the Material Files](#Specify3DFileSaveOptions-DiscardSavingtheMaterialFiles)
        *   1.9.2 [Save Dependencies in the Local Directory](#Specify3DFileSaveOptions-SaveDependenciesintheLocalDirectory)
        *   1.9.3 [Save Dependencies in the MemoryFileSystem Object](#Specify3DFileSaveOptions-SaveDependenciesintheMemoryFileSystemObject)
    *   1.10 [Use of the Google Draco (.drc) Save Options](#Specify3DFileSaveOptions-UseoftheGoogleDraco(.drc)SaveOptions)
    *   1.11 [Use of the RVM Save Options](#Specify3DFileSaveOptions-UseoftheRVMSaveOptions)

 

 

## 3D File Save Options

There are several [`Scene.Save`](http://www.aspose.com/api/net/3d/aspose.threed/scene) method overloads that accept a `SaveOptions` object. This should be an object of a class derived from the `SaveOptions` class. Each save format has a corresponding class that holds save options for that save format, for example, there is `ColladaSaveOptions` for the `FileFormat.Collada` save format.

### Use of the Collada Save Options

The code below shows how to set save options before saving a 3D file to Collada format.

### Use of the Discreet3DS Save Options

The code below shows how to set save options before saving a 3D file to a Discreet 3DS format.

### Use of the FBX Save Options

The code below shows how to set save options before saving a 3D file to an FBX format.

FBXSaveOptions also exposes EnableCompression property which can be used to compress large binary data in the FBX file. Default value of this property is true. Below code snippet explains how can you work with this property while saving a scene.

###   
Use of the Obj Save Options

The code below shows how to set save options before saving a 3D file to an Obj format.

### Use of the STL Save Options

The code below shows how to set save options before saving a 3D file to STL format.

### Use of the U3D Save Options

The code below shows how to set save options before saving a document to U3D format.

### Use of the glTF Save Options

This feature is supported by version 19.8 or greater.

The code below shows how to set save options before saving a document to glTF format.

### PrettyPrint in glTF Save Options

You can also use PrettyPrint property of GLTFSaveOptions class for human-understandable JSON print. The code below shows how to use this functionality. 

### Save Dependencies of a 3D Scene in the Real File System

Developers may require to save all 3D scene dependencies in the real file system. They can define the path of a local directory, save in the MemoryFileSystem object or simply discard dependencies. The `FileSystem` property is added in the all save option classes.

#### Discard Saving the Material Files

#### Save Dependencies in the Local Directory

#### Save Dependencies in the MemoryFileSystem Object

### Use of the Google Draco (.drc) Save Options

The code below shows how to set save options before saving a 3D model to DRC format.

### Use of the RVM Save Options

The code below shows how to set save options before saving a 3D model to RVM format.

