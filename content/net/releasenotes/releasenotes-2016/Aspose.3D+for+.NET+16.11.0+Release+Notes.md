+++
title = "Aspose.3D for .NET 16.11.0 Release Notes" 
description = "" 
weight = 12141 
+++

Aspose.3D for .NET : Aspose.3D for .NET 16.11.0 Release Notes  

# Aspose.3D for .NET : Aspose.3D for .NET 16.11.0 Release Notes


This page contains release notes for [Aspose.3D for .NET 16.11.0](https://www.nuget.org/packages/Aspose.3D/16.11.0).

## Other Improvements and Changes

{{< table style="table-striped" >}}
|Key|Summary|Category|
|:----|:----|:----|
|THREEDNET-219|Directional/spot light in rendering.|New feature|
|THREEDNET-218|Add a new interface to allow user to export dependencies to file system.|New feature|
|THREEDNET-217|Add support of exporting the text/binary glTF.|New feature|
|THREEDNET-215|Add support of importing the binary glTF.|New feature|
|THREEDNET-211|Add support of importing the text-based glTF.|New feature|
{{< /table >}}

### Public API and Backwards Incompatible Changes

See the list of any changes made to the public API such as added, renamed, removed or deprecated members as well as any non-backward compatible change made to Aspose.3D for .NET. If you have concerns about any change listed, please raise it on the [Aspose.3D support forum](http://www.aspose.com/community/forums/aspose.3d-product-family/535/showforum.aspx).

### Adds Aspose.ThreeD.Formats.GLTFLoadOptions Class

We have added `GLTFLoadOptions` class. It defines settings on loading a glTF file.

### Adds Aspose.ThreeD.Formats.GLTFSaveOptions Class

We have added `GLTFSaveOptions` class. It defines settings on saving a glTF file.

### Adds Aspose.ThreeD.Utilities.DummyFileSystem Class

It'll ignore all dependencies while saving the scene using save option classes.

### Adds Aspose.ThreeD.Utilities.LocalFileSystem Class

All dependencies are written to the real file system, this is the default value of each save option classes, developers can use this to redirect the dependencies to a different folder.

### Adds Aspose.ThreeD.Utilities.MemoryFileSystem Class

The `MemoryFileSystem` class intercepts the writing of dependencies, e.g. get the "test.mtl" file content.

### Adds Extension and GLTF Format Entries in the Aspose.ThreeD.FileFormat Class

We have added an `Extension` property and GLTF (GLTF and GLTF\_Binary) format entries for loading and saving purposes.

#### Adds an Extension property in the Aspose.ThreeD.FileFormatType Class

We have added an `Extension` property in the FileFormatType class to get the extension name of the file format.

### Adds FileSystem property in the Aspose.ThreeD.Formats.IOConfig Class

We have added a `FileSystem` property in the IOConfig class to write dependencies.

### Adds AddEntity Method in the Aspose.ThreeD.Node Class

A shortcut way for adding an entity to a node

### Usage Examples

Please check the list of help topics added in the Aspose.3D Wiki docs:

1.  [Use of the glTF Load Options](http://www.aspose.com/docs/display/3dnet/Specify+3D+File+Load+Options#Specify3DFileLoadOptions-UseoftheglTFLoadOptions)
2.  [Use of the glTF Save Options](http://www.aspose.com/docs/display/3dnet/Specify+3D+File+Save+Options#Specify3DFileSaveOptions-UseoftheglTFSaveOptions)
3.  [Save Dependencies of a 3D Scene in the File System](http://www.aspose.com/docs/display/3dnet/Specify+3D+File+Save+Options#Specify3DFileSaveOptions-SaveDependenciesofa3DSceneintheRealFileSystem)

