---
title: Specify 3D File Save Options
type: docs
weight: 10
url: /java/specify-3d-file-save-options/
---

## **3D File Save Options**
There are several Scene.save method overloads that accept a SaveOptions instance. This should be an instance of a class derived from the SaveOptions class. Each save format has a corresponding class that holds save options for that save format, for example there is ColladaSaveOptions for the FileFormat.COLLADA save format.
### **Use of Collada Save Options**
The code below shows how to set save options before saving a 3D file in Collada format.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-ColladaSaveOption.java" >}}
### **Use of Discreet3DS Save Options**
The code below shows how to set save options before saving a 3D file to a Discreet 3DS format.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-Discreet3DSSaveOption.java" >}}
### **Use of the FBX Save Options**
The code below shows how to set save options before saving a 3D file to an FBX format.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-FBXSaveOption.java" >}}
### **Use of OBJ Save Options**
The code below shows how to set save options before saving a 3D file to an Obj format.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-OBJSaveOption.java" >}}
### **Use of STL Save Options**
The code below shows how to set save options before saving a 3D file to STL format.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-STLSaveOption.java" >}}
### **Use of the U3D Save Options**
The code below shows how to set save options before saving a document to U3D format.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-U3DSaveOption.java" >}}
### **Use of the glTF Save Options**
{{% alert color="primary" %}} 

This feature is supported by version 19.8 or greater.

{{% /alert %}} 



The code below shows how to set save options before saving a document to glTF format.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-glTFSaveOption.java" >}}
### **PrettyPrint in glTF Save Options**
You can also use setPrettyPrint method of GLTFSaveOptions class for human-understandable JSON print. The code below shows how to use this functionality. 

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-loadsave-SaveOptions-prettyPrintInGltfSaveOption.java" >}}
### **Save Dependencies of a 3D Scene in the Real File System**
Developers may require to save all dependencies of 3D scene in the real file system. They can define the path of a local directory, save in the MemoryFileSystem object or simply discard dependencies. The FileSystem property is added in the all save option classes.
#### **Discard Saving the Material Files**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-DiscardSavingMaterial.java" >}}
#### **Save Dependencies in the Local Directory**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-SavingDependenciesInLocalDirectory.java" >}}
#### **Save Dependencies in the MemoryFileSystem Instance**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-SavingDependenciesInMemoryFileSystem.java" >}}
### **Use of the Google Draco (.DRC) Save Options**
The code below shows how to set save options before saving a 3D model to DRC format.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-DRCSaveOption.java" >}}
### **Use of RVM Save Options**
The code below shows how to set save options before saving a 3D model to RVM format.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-loadsave-SaveOptions-RVMSaveOptions.java" >}}
