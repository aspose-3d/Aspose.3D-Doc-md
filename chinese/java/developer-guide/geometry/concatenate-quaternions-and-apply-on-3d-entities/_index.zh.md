---
title: 连接四元数并应用于 3D 实体
type: docs
weight: 30
url: /zh/java/concatenate-quaternions-and-apply-on-3d-entities/
description: Aspose.3D for Java 允许开发人员将两个旋转转换合并为一个以四元数表示的旋转转换。
---
{{% alert color="primary" %}} 

Aspose.3D for Java 允许开发人员将两个旋转转换合并为一个以四元数表示的旋转转换。

{{% /alert %}} 
##  **级联四元数**
四元数用于表示 3D 空间中的方向。`Quaternion` 类公开的concat方法可用于组合两个四元数。在此代码示例中，我们组合两个四元数并获得第三个结果四元数，然后将这三个四元数应用于三个圆柱体。
###  **编程示例**
此代码示例将两个四元数组合在一起，并将它们应用于不同的圆柱体。

{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
Scene scene = new Scene();
Quaternion q1 = Quaternion.fromEulerAngle(Math.PI * 0.5, 0, 0);
Vector3.X_AXIS.x = 3;
Quaternion q2 = Quaternion.fromAngleAxis(-Math.PI * 0.5, Vector3.X_AXIS);
// Concatenate q1 and q2. q1 and q2 rotate alone x-axis with same angle but different direction,
// So the concatenated result will be identity quaternion.
Quaternion q3 = q1.concat(q2);
// Create 3 cylinders to represent each quaternion
Node cylinder = scene.getRootNode().createChildNode("cylinder-q1", new Cylinder(0.1, 1, 2));
cylinder.getTransform().setRotation(q1);
cylinder.getTransform().setTranslation(new Vector3(-5, 2, 0));
cylinder = scene.getRootNode().createChildNode("cylinder-q2", new Cylinder(0.1, 1, 2));
cylinder.getTransform().setRotation(q2);
cylinder.getTransform().setTranslation(new Vector3(0, 2, 0));
cylinder = scene.getRootNode().createChildNode("cylinder-q3", new Cylinder(0.1, 1, 2));
cylinder.getTransform().setRotation(q3);
cylinder.getTransform().setTranslation(new Vector3(5, 2, 0));
MyDir = MyDir + "test_out.fbx";
// Save to file
scene.save(MyDir, FileFormat.FBX7400ASCII);
{{< /highlight >}}




**结果3ds MAX**

![todo: 图像 _ alt_text](concatenate-quaternions-and-apply-on-3d-entities_1.png)
