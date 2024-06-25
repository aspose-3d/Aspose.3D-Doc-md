---
title: 在 C# 中指定 3D 文件加载选项
linktitle: 指定 3D 文件加载选项
type: docs
weight: 30
url: /zh/net/specify-3d-file-load-options/
description: 有几个接受LoadOptions对象的Scene.Open方法重载或Scene类构造函数重载。每种加载格式都有一个相应的类，该类保存该加载格式的加载选项。
---
##  **概述**

本文介绍如何在Scene对象内的 C# 中使用各自的加载选项类加载不同类型的 3D 文件，然后再加载 [将其保存为不同的 3D 支持的文件格式](https://docs.aspose.com/3d/net/specify-3d-file-save-options/)。通过加载和保存，您可以执行不同的转换数量。

- 在 C# 中将 FBX 转换为 OBJ
- 在 C# 中将 3DS 转换为 FBX
- 在 C# 中将 U3D 转换为 OBJ
- 在 C# 中将 OBJ 转换为 3DS
- 在 C# 中将X转换为 3DS

##  **3D 文件加载选项**
有几个接受 `LoadOptions` 对象的 [`Scene.Open`](https://reference.aspose.com/3d/net/aspose.threed/scene) 方法重载或Scene类构造函数重载。这应该是从 `LoadOptions` 类派生的类的对象。每个加载格式都有一个对应的类，用于保存该加载格式的加载选项，例如，对于 `FileFormat.Collada` 保存格式，有 `ColladaSaveOptions`。
###  **使用Discreet 3DS 加载选项**
下面的 C# 代码显示了如何在加载谨慎的 3DS 文件之前设置加载选项。

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-Discreet3DSOption.cs" >}}
###  **使用Obj加载选项**
下面的 C# 代码显示了如何在加载 3D Obj文件之前设置加载选项。

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-ObjLoadOption.cs" >}}
###  **STL 加载选项的使用**
下面的 C# 代码显示了如何在加载 STL 文件之前设置加载选项。

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-STLLoadOption.cs" >}}
###  **U3D 加载选项的使用**
下面的 C# 代码显示了如何在加载 U3D 文件之前设置加载选项。

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-U3DLoadOption.cs" >}}
###  **glTF 加载选项的使用**
下面的 C# 代码显示了如何在加载 glTF 文件之前设置加载选项。
####  **翻转V/T纹理坐标**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-glTFLoadOptions.cs" >}}
###  **使用层载荷选项**
下面的 C# 代码显示了如何在加载 PLY 模型之前设置加载选项。

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-PlyLoadOptions.cs" >}}
###  **使用DirectX X加载选项**
下面的 C# 代码显示了如何在加载DirectX X文件之前设置加载选项。

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-XLoadOptions.cs" >}}
###  **使用 RVM 加载选项**
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
###  **使用 FBX 加载选项**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-LoadOptions-FBXLoadOptions.cs" >}}
