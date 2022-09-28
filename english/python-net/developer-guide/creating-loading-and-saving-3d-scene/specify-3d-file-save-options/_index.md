---
title: Specify 3D File Save Options
type: docs
weight: 40
url: /python-net/specify-3d-file-save-options/
description: There are several Scene.Save method overloads that accept a SaveOptions object. Each save format has a corresponding class that holds save options for that save format.
---

## **3D File Save Options**
There are several [`Scene.save`](https://reference.aspose.com/3d/net/aspose.threed/scene) method overloads that accept a `SaveOptions` object. This should be an object of a class derived from the `SaveOptions` class. Each save format has a corresponding class that holds save options for that save format, for example, there is `ColladaSaveOptions` for the `FileFormat.Collada` save format.
### **Use of the Collada Save Options**
The code below shows how to set save options before saving a 3D file to Collada format.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-ColladaSaveOption.py" >}}
### **Use of the Discreet3DS Save Options**
The code below shows how to set save options before saving a 3D file to a Discreet 3DS format.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-Discreet3DSSaveOption.py" >}}
### **Use of the FBX Save Options**
The code below shows how to set save options before saving a 3D file to an FBX format.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-FBXSaveOption.py" >}}

`FBXSaveOptions` also exposes `enable_compression` property which can be used to compress large binary data in the FBX file. Default value of this property is true. Below code snippet explains how can you work with this property while saving a scene.



{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-Save3DScene-Compression.py" >}}
### **Use of the Obj Save Options**
The code below shows how to set save options before saving a 3D file to an Obj format.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-ObjSaveOption.py" >}}
### **Use of the STL Save Options**
The code below shows how to set save options before saving a 3D file to STL format.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-STLSaveOption.py" >}}
### **Use of the U3D Save Options**
The code below shows how to set save options before saving a document to U3D format.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-U3DSaveOption.py" >}}
### **Use of the glTF Save Options**
{{% alert color="primary" %}} 

This feature is supported by version 19.8 or greater.

{{% /alert %}} 



The code below shows how to set save options before saving a document to glTF format.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-glTFSaveOptions.py" >}}
### **PrettyPrint in glTF Save Options**
You can also use PrettyPrint property of GLTFSaveOptions class for human-understandable JSON print. The code below shows how to use this functionality. 

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-PrettyPrintInGltfSaveOption.py" >}}
### **Save Dependencies of a 3D Scene in the Real File System**
Developers may require to save all 3D scene dependencies in the real file system. They can define the path of a local directory, save in the MemoryFileSystem object or simply discard dependencies. The FileSystem property is added in the all save option classes.
#### **Discard Saving the Material Files**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-DiscardSavingMaterial.py" >}}
#### **Save Dependencies in the Local Directory**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-SavingDependenciesInLocalDirectory.py" >}}
#### **Save Dependencies in the MemoryFileSystem Object**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-SavingDependenciesInMemoryFileSystem.py" >}}
### **Use of the Google Draco (.drc) Save Options**
The code below shows how to set save options before saving a 3D model to DRC format.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-DRCSaveOptions.py" >}}
### **Use of the RVM Save Options**
The code below shows how to set save options before saving a 3D model to RVM format.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-SaveOptions-RVMSaveOptions.py" >}}
