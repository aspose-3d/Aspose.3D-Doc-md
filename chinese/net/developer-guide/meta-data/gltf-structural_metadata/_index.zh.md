---
title: "glTF 结构化元数据示例"
type: docs
linkTitle: "glTF 结构化元数据"
description: "本文档演示了如何使用 Aspose.3D for .NET 从 glTF 文件中读取结构化元数据。"
weight: 11
---

# 从 glTF 文件中读取结构化元数据

本示例演示了如何使用 Aspose.3D API 从包含 EXT_structural_metadata 扩展的 glTF 文件中读取结构化元数据。

## 代码说明

以下 C# 代码加载带有结构化元数据的 glTF 场景，然后读取并显示属性表及其属性的信息：

```csharp
// 从文件加载带有 EXT_structural_metadata 的 glTF 场景
var scene = Scene.FromFile("ComplexType.gltf");

// 从场景中加载结构化元数据
var metadata = StructuralMetadata.From(scene);
Console.WriteLine("正在转储输入 glTF 文件中的结构化元数据:");

// 遍历元数据中的所有属性表
foreach (var propTable in metadata.PropertyTables)
{
    // 获取属性表的元类
    Console.WriteLine($"属性表 {propTable.Name}, 类型名称 : {propTable.MetaClass.Name}");

    // 遍历元类中定义的所有属性
    foreach (var propertyDefinition in propTable.MetaClass.Properties)
    {
        // 获取在 EXT_structural_metadata 中定义的属性数据
        object property = propTable.Values[propertyDefinition.Name];
        
        // 转储属性名称、类型和值
        Console.WriteLine($"{propertyDefinition.Name} : {propertyDefinition.Type} = {property}");
    }
}
```

## 核心概念

### 结构化元数据
- `StructuralMetadata` 类提供了对 EXT_structural_metadata 扩展中定义的元数据的访问
- 此扩展允许存储有关 3D 对象的语义信息
- 元数据可以包括定义场景中对象属性的属性表

### 属性表
- 由 `PropertyTable` 类表示
- 每个表都有：
  - 名称
  - 定义结构的元类
  - 包含实际属性数据的值

### 元类
- 由 `MetaClass` 类定义
- 描述属性表的结构
- 包含属性定义的集合
- 每个定义指定：
  - 属性名称
  - 属性类型
  - 其他元数据属性

### 属性访问
- 属性通过属性表的 `Values` 字典访问
- 键是元类中定义的属性名称
- 值会在可能的情况下自动转换为适当的类型

本示例演示了如何使用 Aspose.3D 从 glTF 文件中读取和处理结构化元数据，使开发人员能够访问与 3D 几何体一起存储的丰富语义信息。