+++
title = "Specify 3D File Save Options" 
description = "" 
weight = 16017 
+++

Aspose.3D for Java : Specify 3D File Save Options  

# Aspose.3D for Java : Specify 3D File Save Options


{{< panel title="Contents Summary" style="primary" >}}
*   1 [3D File Save Options](#Specify3DFileSaveOptions-3DFileSaveOptions)
    *   1.1 [Use of Collada Save Options](#Specify3DFileSaveOptions-UseofColladaSaveOptions)
    *   1.2 [Use of Discreet3DS Save Options](#Specify3DFileSaveOptions-UseofDiscreet3DSSaveOptions)
    *   1.3 [Use of the FBX Save Options](#Specify3DFileSaveOptions-UseoftheFBXSaveOptions)
    *   1.4 [Use of OBJ Save Options](#Specify3DFileSaveOptions-UseofOBJSaveOptions)
    *   1.5 [Use of STL Save Options](#Specify3DFileSaveOptions-UseofSTLSaveOptions)
    *   1.6 [Use of the U3D Save Options](#Specify3DFileSaveOptions-UseoftheU3DSaveOptions)
    *   1.7 [Use of the glTF Save Options](#Specify3DFileSaveOptions-UseoftheglTFSaveOptions)
    *   1.8 [PrettyPrint in glTF Save Options](#Specify3DFileSaveOptions-PrettyPrintinglTFSaveOptions)
    *   1.9 [Save Dependencies of a 3D Scene in the Real File System](#Specify3DFileSaveOptions-SaveDependenciesofa3DSceneintheRealFileSystem)
        *   1.9.1 [Discard Saving the Material Files](#Specify3DFileSaveOptions-DiscardSavingtheMaterialFiles)
        *   1.9.2 [Save Dependencies in the Local Directory](#Specify3DFileSaveOptions-SaveDependenciesintheLocalDirectory)
        *   1.9.3 [Save Dependencies in the MemoryFileSystem Instance](#Specify3DFileSaveOptions-SaveDependenciesintheMemoryFileSystemInstance)
    *   1.10 [Use of the Google Draco (.DRC) Save Options](#Specify3DFileSaveOptions-UseoftheGoogleDraco(.DRC)SaveOptions)
    *   1.11 [Use of RVM Save Options](#Specify3DFileSaveOptions-UseofRVMSaveOptions)
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

