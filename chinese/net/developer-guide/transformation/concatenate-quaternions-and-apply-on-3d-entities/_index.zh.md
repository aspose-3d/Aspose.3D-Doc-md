---
title: 连接四元数并应用于 3D 实体
type: docs
weight: 50
url: /zh/net/concatenate-quaternions-and-apply-on-3d-entities/
description: Aspose.3D for .NET 允许开发人员将两个旋转转换合并为一个以四元数表示的旋转转换。
---
{{% alert color="primary" %}} 

[Aspose.3D for .NET](https://www.aspose.com/products/3d) 允许开发人员将两个旋转转换合并为一个以四元数表示的转换。

{{% /alert %}} 
##  **级联四元数**
四元数用于表示 3D 空间中的方向。由 [`Quaternion`](https://reference.aspose.com/3d/net/aspose.threed.utilities/quaternion) 类公开的 `Concat` 方法可用于组合两个四元数。在此代码示例中，我们组合两个四元数并获得第三个结果四元数，然后将这三个四元数应用于三个圆柱体。
###  **编程示例**
此代码示例将两个四元数组合在一起，并将它们应用于不同的圆柱体。

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET

            Scene scene = new Scene();

            Quaternion q1 = Quaternion.FromEulerAngle(Math.PI * 0.5, 0, 0);
            Quaternion q2 = Quaternion.FromAngleAxis(-Math.PI * 0.5, Vector3.XAxis);
            // Concatenate q1 and q2. q1 and q2 rotate alone x-axis with same angle but different direction,
            // So the concatenated result will be identity quaternion.
            Quaternion q3 = q1.Concat(q2);

            // Create 3 cylinders to represent each quaternion
            Node cylinder = scene.RootNode.CreateChildNode("cylinder-q1", new Cylinder(0.1, 1, 2));
            cylinder.Transform.Rotation = q1;
            cylinder.Transform.Translation = new Vector3(-5, 2, 0);

            cylinder = scene.RootNode.CreateChildNode("cylinder-q2", new Cylinder(0.1, 1, 2));
            cylinder.Transform.Rotation = q2;
            cylinder.Transform.Translation = new Vector3(0, 2, 0);

            cylinder = scene.RootNode.CreateChildNode("cylinder-q3", new Cylinder(0.1, 1, 2));
            cylinder.Transform.Rotation = q3;
            cylinder.Transform.Translation = new Vector3(5, 2, 0);
            // Save to file
            scene.Save("test_out.fbx");

{{< /highlight >}}


**结果3ds MAX**

![todo: 图像 _ alt_text](concatenate-quaternions-and-apply-on-3d-entities_1.png)
