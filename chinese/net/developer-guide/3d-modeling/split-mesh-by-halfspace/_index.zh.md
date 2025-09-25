---
title: "如何在 Aspose.3D 中通过半空间分割网格"
type: docs
linkTitle: "Split Mesh by HalfSpace"
description: "了解如何使用 HalfSpace 平面在 Aspose.3D 中分割 3D 网格。"
weight: 10
---

# 使用半空间分割网格

本教程演示如何使用 Aspose.3D 执行使用半空间平面的网格分割操作。此技术可用于根据空间标准提取 3D 模型的部分。

## 理解半空间操作

半空间表示由平面分割的无限空间。结合 Aspose.3D 的布尔运算，它可以允许您提取相对于定义的平面的一侧的网格部分。

### 关键概念：
- **半空间**: 表示由平面分割的无限空间
- **布尔运算**: 用于相对于半空间提取网格部分
- **平面方程**: 定义为 ax + by + cz + d = 0，其中 (a,b,c) 是法向量
- **正侧**: 平面法向量指向的空间部分

## 代码示例：使用半空间分割网格

以下 C# 代码演示如何创建简单的盒状网格并使用半空间平面分割它：

```csharp
using System;
using Aspose.ThreeD;
using Aspose.ThreeD.Entities;  // Contains HalfSpace and BooleanOperator classes
using Aspose.ThreeD.Utilities; // Contains Vector3 and Plane utilities

class MeshBooleanWithHalfSpace
{
    public static void Execute()
    {
        // 创建新的 3D 场景
        Scene scene = new Scene();
        
        // 创建盒状网格（默认尺寸为 2x2x2）
        Mesh boxMesh = (new Box()).ToMesh();
        Node boxNode = scene.RootNode.CreateChildNode("Box", boxMesh);
        
        // 创建半空间切割平面
        HalfSpace halfSpace = new HalfSpace();
        
        // 定义平面方程：ax + by + cz + d = 0
        // 使用法向量指向 Z 方向
        halfSpace.Plane = new Plane(new Vector3(0, 0, 1), 0);
        
        // 放置半空间（创建节点和变换）
        Node halfSpaceNode = scene.RootNode.CreateChildNode("HalfSpace", halfSpace);
        halfSpaceNode.Transform.Translation = new Vector3(0, 0, 0.5);  // 放置在 z=0.5 处
        
        // 执行布尔分割操作
        Node splitResult = BooleanOperator.Split(boxNode, halfSpaceNode);
        
        // 将结果添加到场景并保存
        scene.RootNode.CreateChildNode("SplitResult", splitResult.Entity);
        scene.Save("halfspace_split_result.obj", FileFormat.WavefrontOBJ);
        
        Console.WriteLine("使用半空间分割网格完成成功。");
    }
}
```

## 代码说明

### 命名空间要求
```csharp
using Aspose.ThreeD;
using Aspose.ThreeD.Entities;  // Contains HalfSpace and BooleanOperator classes
using Aspose.ThreeD.Utilities; // Contains Vector3 and Plane utilities
```

### 创建几何体
1. **场景初始化**: `Scene scene = new Scene();`
2. **盒状创建**: `(new Box()).ToMesh()` 创建一个标准立方体
3. **节点层次结构**: 网格通过子节点添加到场景中

### 定义切割平面
1. **平面定义**:
   ```csharp
   halfSpace.Plane = new Plane(new Vector3(0, 0, 1), 0);
   ```
   - 创建 XY 水平平面在 z=0 处
   - 法向量 (0,0,1) 指向上方

2. **放置**:
   ```csharp
   halfSpaceNode.Transform.Translation = new Vector3(0, 0, 0.5);
   ```
   - 将切割平面移动到 z=0.5
   - 影响保留的网格部分的哪一部分

### 执行操作
```csharp
Node splitResult = BooleanOperator.Split(boxNode, halfSpaceNode);
```
- 返回平面正侧的网格部分
- 结果添加到场景层次结构中

### 保存结果
```csharp
scene.Save("halfspace_split_result.obj", FileFormat.WavefrontOBJ);
```
- 支持的格式包括 OBJ、STL、FBX、GLTF 等
- 仅保存分割片段，而不是原始网格

## 可视化操作

### 原始盒状尺寸：
- 从 (-1,-1,-1) 到 (1,1,1) 跨越
- 位于原点

### 具有在 z=0.5 处的平面：
- 保留 z > 0.5 处的部分（盒子的顶部）
- 丢弃 z < 0.5 处的部分（盒子的底部）

## 高级用法

### 获取切割的两个侧面
```csharp
// 原始分割（正侧）
Node positiveFragment = BooleanOperator.Split(boxNode, halfSpaceNode);

// 反转平面以获取负侧
halfSpace.Plane = new Plane(new Vector3(0, 0, -1), 0);
Node negativeFragment = BooleanOperator.Split(boxNode, halfSpaceNode);
```

### 调整切割平面
```csharp
// 不同的方向 - 倾斜切割
halfSpace.Plane = new Plane(new Vector3(0.707, 0, 0.707), 0);
halfSpaceNode.Transform.Translation = new Vector3(0, 0, 1);
```

此实现演示了 Aspose.3D 的网格分割功能的关键功能，使用半空间平面，允许根据空间标准精确提取 3D 几何体。
