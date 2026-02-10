---
title: 创建并读取现有 3D 场景
type: docs
weight: 10
url: /zh/net/create-and-read-an-existing-3d-scene/
description: Aspose。3D API 支持从头开始创建新的 3D 场景，然后以任何支持的文件格式保存。开发人员还可以加载现有的 3D 场景以进行修改、添加或处理。
---
##  **概述**
本文介绍了以下使用 C# 3D 文件格式操作库的主题。
- 从头开始在 C# 中创建一个空的 3D 场景
- 读取或加载 C# 中现有的 3D 场景
- 使用 C# 以支持的 3D 格式保存 3D 场景
- 使用 C# 中的 3D 场景属性

##  **创建一个空的 3D 场景并以支持的 3D 文件格式保存**
Aspose。3D API 支持从头开始创建新的 3D 场景，然后以任何支持的文件格式保存。开发人员还可以加载现有的 3D 场景以进行修改、添加或处理。

###  **创建 3D 场景文档**
请按照 C# 中的以下步骤使用 Aspose.3D api创建 3D 场景文档:

1. 创建表示 3D 场景文档的 [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) 类的实例。
1. 通过调用Scene类对象的 [`Save`](https://reference.aspose.com/3d/net/aspose.threed/scene/methods/save) 方法生成 3D Scene文档。

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET

// Create an object of the Scene class
Scene scene = new Scene();
// Save 3D scene document
scene.Save("document.fbx");

{{< /highlight >}}

##  **正在读取 3D 场景**
使用 Aspose.3D API，开发人员可以加载所有受支持的 3D 文档。`Scene` 类的可用构造函数允许这样做，并且它们接受有效的文件路径字符串。支持的可读文件格式如下:

1. FBX 7.5 (ASCII，二进制)
1. FBX 7.4 (ASCII，二进制)
1. FBX 7.3 (ASCII，二进制)
1. FBX 7.2 (ASCII，二进制)
1. FBX 6.1 (ASCII，二进制)
1. STL (ASCII，二进制)
1. WavefrontOBJ
1. Discreet3DS
1. Universal3D
1. Collada
1. glTF (ASCII，二进制)
1. Maya (ASCII，二进制)
1. OpenUSD (USD, USDZ)
1. 搅拌机
1. DXF
1. PLY (ASCII，二进制)
1. X (ASCII，二进制)
1. Draco
1. 3MF
1. RVM (文本，二进制)
1. ASE

`Scene` 类的构造函数在内部检测 3D 文档格式。

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// The path to the documents directory.

// Initialize a Scene class object
Scene scene = new Scene();
// Load an existing 3D document
scene.Open("document.fbx");


{{< /highlight >}}

##  **使用 3D 场景属性**
Aspose.3D API 允许您使用场景的子节点读取 3D 场景属性。下面的 C# 代码示例演示了此功能的用法。

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
Scene scene = Scene.FromFile("EmbeddedTexture.fbx");
Material material = scene.RootNode.ChildNodes[0].Material;
PropertyCollection props = material.Properties;
//List all properties using foreach
foreach (var prop in props)
{
    Console.WriteLine("{0} = {1}", prop.Name, prop.Value);
}
//or using ordinal for loop
for (int i = 0; i < props.Count; i++)
{
    var prop = props[i];
    Console.WriteLine("{0} = {1}", prop.Name, prop.Value);
}
//Get property value by name
var diffuse = props["Diffuse"];
Console.WriteLine(diffuse);
//modify property value by name
props["Diffuse"] = new Vector3(1, 0, 1);
//Get property instance by name
Property pdiffuse = props.FindProperty("Diffuse");
Console.WriteLine(pdiffuse);
//Since Property is also inherited from A3DObject
//It's possible to get the property of the property
Console.WriteLine("Property flags = {0}", pdiffuse.GetProperty("flags"));
//and some properties that only defined in FBX file:
Console.WriteLine("Label = {0}", pdiffuse.GetProperty("label"));
Console.WriteLine("Type Name = {0}", pdiffuse.GetProperty("typeName"));
//so traversal on property's property is possible
foreach (var pp in pdiffuse.Properties)
{
    Console.WriteLine("Diffuse.{0} = {1}", pp.Name, pp.Value);
}

{{< /highlight >}}
