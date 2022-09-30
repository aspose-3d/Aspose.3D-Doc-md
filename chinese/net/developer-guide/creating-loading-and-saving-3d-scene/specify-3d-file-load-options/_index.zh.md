---
title: 在C#中指定3D文件加载选项
linktitle: 指定3D文件加载选项
type: docs
weight: 30
url: /zh/net/specify-3d-file-load-options/
description: 有几个接受LoadOptions对象的Scene.Open方法重载或Scene类构造函数重载。每种加载格式都有一个相应的类，该类保存该加载格式的加载选项。
---
## **概述**

本文介绍了如何在场景对象内的C#中使用它们各自的加载选项类加载不同类型的3D文件，然后您可以[将其保存在不同3D支持的文件格式中](https://docs.aspose.com/3d/net/specify-3d-file-save-options/)。通过加载和保存，您可以执行许多不同的转换，例如

- 在C#中将FBX转换为OBJ
- 在C#中将3DS转换为FBX
- 在C#中将U3D转换为OBJ
- 在C#中将OBJ转换为3DS
- 在C#中将X转换为3DS

## **3D文件加载选项**
有几个[`Scene.Open`](https://reference.aspose.com/3d/net/aspose.threed/scene)方法重载或场景类构造函数重载接受`LoadOptions`对象。这应该是从`LoadOptions`类派生的类的对象。每个加载格式都有一个相应的类，该类保存该加载格式的加载选项，例如，存在`FileFormat.Collada`保存格式的`ColladaSaveOptions`。
### **使用谨慎的3DS加载选项**
下面的C#代码显示了如何在加载谨慎的3DS文件之前设置加载选项。

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-Discreet3DSOption.cs" >}}
### **使用Obj加载选项**
下面的C#代码显示了如何在加载3D Obj文件之前设置加载选项。

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-ObjLoadOption.cs" >}}
### **使用STL加载选项**
下面的C#代码显示了如何在加载STL文件之前设置加载选项。

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-STLLoadOption.cs" >}}
### **使用U3D加载选项**
下面的C#代码显示了如何在加载U3D文件之前设置加载选项。

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-U3DLoadOption.cs" >}}
### **使用glTF加载选项**
下面的C#代码显示了如何在加载glTF文件之前设置加载选项。
#### **翻转V/T纹理坐标**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-glTFLoadOptions.cs" >}}
### **使用层载荷选项**
下面的C#代码显示了如何在加载PLY模型之前设置加载选项。

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-PlyLoadOptions.cs" >}}
### **使用DirectX X加载选项**
下面的C#代码显示了如何在加载DirectX X文件之前设置加载选项。

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-XLoadOptions.cs" >}}
### **使用RVM加载选项**
**C#**

{{< highlight "java" >}}

 // set load options of RVM

Scene scene = new Scene();

var opt = new RvmLoadOptions()

{

    CylinderRadialSegments = 32,

    DishLatitudeSegments = 16,

    DishLongitudeSegments = 24,

    TorusTubularSegments = 40

};

// import RVM

scene.Open("LAD-TOP.rvm", opt);

// save in the OBJ format

scene.Save("LAD-TOP.obj", FileFormat.WavefrontOBJ);

{{< /highlight >}}
### **使用FBX加载选项**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-FBXLoadOptions.cs" >}}
