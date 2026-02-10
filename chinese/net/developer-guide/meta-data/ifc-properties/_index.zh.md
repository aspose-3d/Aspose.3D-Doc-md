---
description: "本文档页面演示了如何使用 Aspose.3D for .NET 从 IFC 文件读取属性。"
linkTitle: "IFC 属性支持"
title: "IFC 属性支持"
type: docs
weight: 14
---
## 概览

IFC 属性支持是 Aspose.3D 中的一项功能，允许开发者读取 IFC 文件中定义的属性集和构件数量。这些属性存储在 `IFCPROPERTYSET` 和 `IFCELEMENTQUANTITY` 实体中，可通过 `A3DObject.GetProperty` 方法访问。

## 什么是 IFC 属性支持？

在 IFC 模式中，建筑构件可以关联属性集（`IFCPROPERTYSET`）和构件数量（`IFCELEMENTQUANTITY`）。Aspose.3D 将它们映射为通用属性接口，并通过 `A3DObject.GetProperty(string propertyName)` 暴露。这样即可直接从 3D 模型中获取防火等级、热传递率或材料数量等数值。

## 为什么使用 IFC 属性支持？

* 在无需手动解析 IFC 文件的情况下访问丰富的语义数据。  
* 为后续流程提供支持，例如成本估算、合规检查或数据导出。  
* 在单一工作流中结合几何信息和非几何信息。

## Aspose.3D 支持

以下 C# 示例演示了如何加载 IFC 文件并读取属性：

```csharp
using Aspose.ThreeD;

var scene = Scene.FromFile("sample.ifc");

// 查找特定构件，例如墙体
var wallNode = scene.RootNode.Children.FirstOrDefault(n => n.Name == "Wall_123");

// 获取属性值
if (wallNode != null)
{
    // IFC 文件中定义的属性名称
    var fireRating = wallNode.GetProperty("ifc:FireRating");
    Console.WriteLine($"Fire Rating: {fireRating}");

    // 构件数量示例
    var volume = wallNode.GetProperty("ifc:GrossVolume");
    Console.WriteLine($"Gross Volume: {volume}");
}
```

### 注意事项

* IFC 文件中定义的属性名称带有 `ifc:` 前缀，以避免与本机属性冲突。  
* 属性名称区分大小写，必须与 IFC 文件中定义的名称完全匹配。  
* `GetProperty` 返回 `object`；需要时将其转换为相应的类型（例如 `double`、`string`）。  
* 此示例代码演示了从 `Node` 读取属性；实际上，任何继承自 `A3DObject` 的子类都可以使用 `GetProperty`。  
* 若属性不存在，`GetProperty` 返回 `null`。

## 参考资料

* [官方 Aspose.3D IFC 文档](/3d/net/supported-file-formats/ifc)  
* 链接至 [`Aspose.ThreeD.A3DObject`](https://reference.aspose.com/3d/net/aspose.threed/a3dobject/)  
* IFC 规范中关于 `IFCPROPERTYSET` 和 `IFCELEMENTQUANTITY` 的说明