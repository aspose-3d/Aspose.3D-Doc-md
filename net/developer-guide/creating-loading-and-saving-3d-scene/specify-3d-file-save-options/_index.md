---
title: Specify 3D File Save Options
type: docs
weight: 40
url: /net/specify-3d-file-save-options/
---

## **3D File Save Options**
There are several [Scene.Save](https://apireference.aspose.com/3d/net/aspose.threed/scene) method overloads that accept a SaveOptions object. This should be an object of a class derived from the SaveOptions class. Each save format has a corresponding class that holds save options for that save format, for example, there is ColladaSaveOptions for the FileFormat.Collada save format.
### **Use of the Collada Save Options**
The code below shows how to set save options before saving a 3D file to Collada format.

{{< gist "aspose-3d" "631532eeb21c3374f2ed" "Examples-CSharp-Loading-and-Saving-SaveOptions-ColladaSaveOption.cs" >}}
### **Use of the Discreet3DS Save Options**
The code below shows how to set save options before saving a 3D file to a Discreet 3DS format.

{{< gist "aspose-3d" "631532eeb21c3374f2ed" "Examples-CSharp-Loading-and-Saving-SaveOptions-Discreet3DSSaveOption.cs" >}}
### **Use of the FBX Save Options**
The code below shows how to set save options before saving a 3D file to an FBX format.

{{< gist "aspose-3d" "631532eeb21c3374f2ed" "Examples-CSharp-Loading-and-Saving-SaveOptions-FBXSaveOption.cs" >}}

FBXSaveOptions also exposes EnableCompression property which can be used to compress large binary data in the FBX file. Default value of this property is true. Below code snippet explains how can you work with this property while saving a scene.



{{< gist "aspose-3d" "631532eeb21c3374f2ed" "Examples-CSharp-Loading-and-Saving-Save3DScene-Compression.cs" >}}
### **Use of the Obj Save Options**
The code below shows how to set save options before saving a 3D file to an Obj format.

{{< gist "aspose-3d" "631532eeb21c3374f2ed" "Examples-CSharp-Loading-and-Saving-SaveOptions-ObjSaveOption.cs" >}}
### **Use of the STL Save Options**
The code below shows how to set save options before saving a 3D file to STL format.

{{< gist "aspose-3d" "631532eeb21c3374f2ed" "Examples-CSharp-Loading-and-Saving-SaveOptions-STLSaveOption.cs" >}}
### **Use of the U3D Save Options**
The code below shows how to set save options before saving a document to U3D format.

{{< gist "aspose-3d" "631532eeb21c3374f2ed" "Examples-CSharp-Loading-and-Saving-SaveOptions-U3DSaveOption.cs" >}}
### **Use of the glTF Save Options**
{{% alert color="primary" %}} 

This feature is supported by version 19.8 or greater.

{{% /alert %}} 



The code below shows how to set save options before saving a document to glTF format.

{{< gist "aspose-3d" "631532eeb21c3374f2ed" "Examples-CSharp-Loading-and-Saving-SaveOptions-glTFSaveOptions.cs" >}}
### **PrettyPrint in glTF Save Options**
You can also use PrettyPrint property of GLTFSaveOptions class for human-understandable JSON print. The code below shows how to use this functionality. 

{{< gist "aspose-com-gists" "15575b5bc038760ad09b3859ce2e3194" "Examples-CSharp-Loading-and-Saving-SaveOptions-PrettyPrintInGltfSaveOption.cs" >}}
### **Save Dependencies of a 3D Scene in the Real File System**
Developers may require to save all 3D scene dependencies in the real file system. They can define the path of a local directory, save in the MemoryFileSystem object or simply discard dependencies. The FileSystem property is added in the all save option classes.
#### **Discard Saving the Material Files**
{{< gist "aspose-3d" "631532eeb21c3374f2ed" "Examples-CSharp-Loading-and-Saving-SaveOptions-DiscardSavingMaterial.cs" >}}
#### **Save Dependencies in the Local Directory**
{{< gist "aspose-3d" "631532eeb21c3374f2ed" "Examples-CSharp-Loading-and-Saving-SaveOptions-SavingDependenciesInLocalDirectory.cs" >}}
#### **Save Dependencies in the MemoryFileSystem Object**
{{< gist "aspose-3d" "631532eeb21c3374f2ed" "Examples-CSharp-Loading-and-Saving-SaveOptions-SavingDependenciesInMemoryFileSystem.cs" >}}
### **Use of the Google Draco (.drc) Save Options**
The code below shows how to set save options before saving a 3D model to DRC format.

{{< gist "aspose-3d" "631532eeb21c3374f2ed" "Examples-CSharp-Loading-and-Saving-SaveOptions-DRCSaveOptions.cs" >}}
### **Use of the RVM Save Options**
The code below shows how to set save options before saving a 3D model to RVM format.

{{< gist "aspose-com-gists" "15575b5bc038760ad09b3859ce2e3194" "Examples-CSharp-Loading-and-Saving-SaveOptions-RVMSaveOptions.cs" >}}
