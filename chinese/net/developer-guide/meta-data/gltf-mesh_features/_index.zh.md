---
title: glTF 网格功能示例
type: docs
linkTitle: glTF 网格功能
description: 本文档页面演示了如何使用 Aspose.3D for .NET 创建包含 EXT_mesh_features 的 glTF 文件。
weight: 10
---

# 使用 EXT_mesh_features 创建 glTF 文件

本示例演示如何使用 Aspose.3D API 创建带有 EXT_mesh_features 扩展的 glTF 文件。

## 代码解释

以下 C# 代码创建了一个带有控制点和多边形的网格，然后在保存到 glTF 文件之前，将特征 ID 添加到控制点：

```csharp
// 此示例将创建一个带有 EXT_mesh_features 的 glTF 文件
// 首先我们创建一个网格
var mesh = new Mesh();

// 向网格添加控制点（顶点）
// 第一组四个点在 y=1 的 XY 平面上创建一个正方形
mesh.ControlPoints.Add(new Vector4(0, 1, 0));  // 点 0
mesh.ControlPoints.Add(new Vector4(2, 1, 0));  // 点 1
mesh.ControlPoints.Add(new Vector4(2, 2, 0));  // 点 2
mesh.ControlPoints.Add(new Vector4(1, 2, 0));  // 点 3

// 第二组四个点在 y=0 的 XY 平面上创建另一个正方形
mesh.ControlPoints.Add(new Vector4(3, 0, 0));  // 点 4
mesh.ControlPoints.Add(new Vector4(4, 0, 0));  // 点 5
mesh.ControlPoints.Add(new Vector4(4, 1, 0));  // 点 6
mesh.ControlPoints.Add(new Vector4(3, 1, 0));  // 点 7

// 从控制点创建三角形面（多边形）
// 第一个正方形（点 0-3）被分成两个三角形
mesh.CreatePolygon(0, 1, 2);  // 三角形 0-1-2
mesh.CreatePolygon(0, 2, 3);  // 三角形 0-2-3

// 第二个正方形（点 4-7）也被分成两个三角形
mesh.CreatePolygon(4, 5, 6);  // 三角形 4-5-6
mesh.CreatePolygon(4, 6, 7);  // 三角形 4-6-7

// 然后我们创建一个用户数据元素来存储特征 ID
// 这会将特征 ID 与控制点关联
var featureId = (VertexElementUserData)mesh.CreateElement(
    VertexElementType.UserData,  // 元素类型
    MappingMode.ControlPoint,   // 应用于控制点
    ReferenceMode.Direct        // 直接映射（非索引）
);

// 为每个控制点分配特征 ID
// 前四个点获得 ID 0，后四个点获得 ID 1
featureId.Data = new float[] { 0, 0, 0, 0, 1, 1, 1, 1 };

// 设置符合 EXT_mesh_features 规范的特殊属性名称
// 格式 _FEATURE_ID_<n> 由 glTF 导出器识别
featureId.Name = "_FEATURE_ID_0";

// 将网格保存到 glTF 二进制文件 (GLB)
// 导出器将自动生成 EXT_mesh_features 扩展数据
// 使用相对路径作为输出文件
(new Scene(mesh)).Save("mesh_feature.glb");
```

## 关键概念

### 网格创建
- `Mesh` 类表示多边形网格几何体
- 控制点定义网格的顶点
- `CreatePolygon` 方法在控制点之间创建三角形面

### 特征 ID
- 特征 ID 允许在网格中对几何体进行分组
- 通过 `VertexElementUserData` 和特殊的命名约定实现
- `_FEATURE_ID_0` 表示这是一个特征 ID 流
- 可以创建具有递增索引的多个特征 ID 流

### 数据分配
- 特征 ID 存储为浮点值
- 每个控制点获得相应特征 ID 值
- 在此示例中，我们使用两个不同的特征 ID：0 和 1

### 文件导出
- 保存到 GLB 格式会保留所有功能，包括 EXT_mesh_features
- Aspose.3D 自动处理扩展生成
- 结果文件包含有关网格功能的元数据
- 使用相对路径使代码更具可移植性，并在不同的环境中更容易运行

此示例演示了如何使用 Aspose.3D 创建使用 EXT_mesh_features 扩展进行高级 3D 数据表示的 glTF 文件。