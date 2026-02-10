---
title: IFC集团支持
type: docs
linkTitle: IFC集团支持
description: 此文档页面演示如何使用 Aspose.3D for .NET 从 IFC 文件读取语义层次结构。
weight: 14
i18n_hash: 34bf3dc260d3bf202703b6f70981f703
---

# IFC 组支持

## 概述

IFC 组是 Aspose.3D 中新引入的功能，允许开发者处理 IFC 文件中定义的语义组。与传统的几何层次结构不同，IFC 组提供了一种以有意义的分组方式表示建筑元素的方法，从而实现更丰富的数据提取和操作。

## 什么是 IFC 组？

在 IFC（Industry Foundation Classes）格式中，组用于创建基于语义的层次结构，将相关实体（例如墙体、门）归于同一标识符下。Aspose.3D 通过 [`Group`](https://reference.aspose.com/3d/net/aspose.threed/group/) 类公开这些组，允许访问组的名称、语义信息以及子节点。

## 为什么使用 IFC 组？

使用 IFC 组为原本纯几何的场景图添加语义上下文，使得基于真实世界含义查询、过滤和处理建筑元素更加容易。它简化了提取特定建筑组件、应用材质覆盖或生成详细报告等任务。

## Aspose.3D 支持

Aspose.3D 在 .NET API 中提供对 IFC 组的完整支持。以下章节展示如何启用并使用 IFC 组。

### 访问组信息

```csharp
// 加载 IFC 文件
var scene = Aspose.ThreeD.Scene.FromFile("model.ifc");
// 遍历组
foreach(Group group in scene2.Library.Where(obj => obj is Group))
{
    Console.WriteLine($"Group Name: {group.Name}");
    Console.WriteLine($" Sub Groups: {group.Groups.Count}");
    Console.WriteLine($" Associated Nodes: {group.Nodes.Count}");
}
```

## 示例代码

以下端到端示例加载 IFC 文件，并打印语义层次结构：

```csharp
using Aspose.ThreeD;

var scene = Scene.FromFile("sample.ifc");
scene.Open("sample.ifc", loadOptions);

void PrintGroup(Group group, string indent = "")
{
    foreach (var child in group.Groups)
    {
        Console.WriteLine($"{indent}{child.Name}");
        PrintGroup(child, indent + "  ");
    }
}

foreach(Group group in scene2.Library.Where(obj => obj is Group))
{
    PrintGroup(group);
}
```

## 参考资料

* [官方 Aspose.3D IFC 文档链接](/3d/net/supported-file-formats/ifc)
* [`Aspose.ThreeD.Group` 链接](https://reference.aspose.com/3d/net/aspose.threed/group/)
* [IFC 规范链接](https://technical.buildingsmart.org/standards/ifc/ifc-schema-specifications/)