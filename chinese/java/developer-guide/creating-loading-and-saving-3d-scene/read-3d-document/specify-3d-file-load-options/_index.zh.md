---
title: 指定3D文件加载选项
type: docs
weight: 10
url: /zh/java/specify-3d-file-load-options/
description: 有几个接受loadopons实例的Scene.open方法重载或Scene类构造函数重载。
---
## **3D文件加载选项**
有几个接受loadopons实例的Scene.open方法重载或Scene类构造函数重载。这应该是从LoadOptions类派生的类的实例。每种加载格式都有一个相应的类，该类保存该加载格式的加载选项，例如，FileFormat.COLLADA保存格式有colladasveoptions。
### **使用谨慎的3DS加载选项**
下面的代码显示了如何在加载谨慎的3DS文件之前设置加载选项。

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-Discreet3DSLoadOption.java" >}}
### **使用Obj加载选项**
下面的代码显示了如何在加载3D Obj文件之前设置加载选项。

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-OBJLoadOption.java" >}}
### **使用STL加载选项**
下面的代码显示了如何在加载STL文件之前设置加载选项。

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-STLLoadOption.java" >}}
### **使用U3D加载选项**
下面的代码显示了如何在加载U3D文件之前设置加载选项。

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-U3DLoadOption.java" >}}
### **使用glTF加载选项**
下面的代码显示了如何在加载glTF文件之前设置加载选项。
#### **翻转V/T纹理坐标**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-glTFLoadOptions.java" >}}
### **使用层载荷选项**
下面的代码显示了如何在加载PLY模型之前设置加载选项。

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-PLYLoadOption.java" >}}
### **使用DirectX X加载选项**
下面的代码显示了如何在加载DirectX X文件之前设置加载选项。

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-XLoadOption.java" >}}
### **使用FBX加载选项**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-loadsave-LoadOptions-FBXLoadOptions.java" >}}
