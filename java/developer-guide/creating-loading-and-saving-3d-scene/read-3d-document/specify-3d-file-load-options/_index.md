---
title: Specify 3D File Load Options
type: docs
weight: 10
url: /java/specify-3d-file-load-options/
description: There are several Scene.open method overloads or Scene class constructor overloads that accept LoadOptions instance.
---

## **3D File Load Options**
There are several Scene.open method overloads or Scene class constructor overloads that accept LoadOptions instance. This should be an instance of a class derived from the LoadOptions class. Each load format has a corresponding class that holds load options for that load format, for example there is ColladaSaveOptions for the FileFormat.COLLADA save format.
### **Use of the Discreet 3DS Load Options**
The code below shows how to set load options before loading a Discreet 3DS file.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-Discreet3DSLoadOption.java" >}}
### **Use of the Obj Load Options**
The code below shows how to set load options before loading an 3D Obj file.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-OBJLoadOption.java" >}}
### **Use of the STL Load Options**
The code below shows how to set load options before loading an STL file.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-STLLoadOption.java" >}}
### **Use of the U3D Load Options**
The code below shows how to set load options before loading a U3D file.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-U3DLoadOption.java" >}}
### **Use of the glTF Load Options**
The code below shows how to set load options before loading a glTF file.
#### **Flip the V/T Texture Coordinate**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-glTFLoadOptions.java" >}}
### **Use of the Ply Load Options**
The code below shows how to set load options before loading a PLY model.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-PLYLoadOption.java" >}}
### **Use of the DirectX X Load Options**
The code below shows how to set load options before loading a DirectX X file.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-XLoadOption.java" >}}
### **Use FBX Load Options**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-loadsave-LoadOptions-FBXLoadOptions.java" >}}
