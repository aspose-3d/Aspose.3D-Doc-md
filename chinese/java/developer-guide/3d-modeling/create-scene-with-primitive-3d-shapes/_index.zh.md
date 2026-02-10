---
title: 创建具有原始 3D 形状的场景
type: docs
weight: 20
url: /zh/java/create-scene-with-primitive-3d-shapes/
description: Aspose.3D for Java API 支持基元 3D 形状。所有参数化图元将自动转换为网格，同时以任何支持的输出文件格式保存。
---
{{% alert color="primary" %}} 

Aspose.3D for Java API 支持基元 3D 形状。所有参数化图元将自动转换为网格，同时以任何支持的输出文件格式保存。

{{% /alert %}} 
##  **从原始 3D 形状生成场景**
建模是纯粹的创建过程，Aspose.3D API 支持创建具有原始 3D 形状的场景。
###  **编程示例**
此代码示例创建一个包含原始 3D 形状的场景，并将其保存在 FBX 文件中。

{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// Initialize a Scene object
Scene scene = new Scene();
// Create a Box model
scene.getRootNode().createChildNode("box", new Box());
// Create a Cylinder model
scene.getRootNode().createChildNode("cylinder", new Cylinder());
// Save drawing in the FBX format
MyDir = MyDir + RunExamples.getOutputFilePath("test.fbx");
scene.save(MyDir, FileFormat.FBX7500ASCII);
{{< /highlight >}}
