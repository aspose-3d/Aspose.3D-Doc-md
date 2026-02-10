---
title: 在 C# 的 PDF 中保存 3D 场景
linktitle: 在 PDF 中保存 3D 场景
type: docs
weight: 60
url: /zh/net/save-a-3d-scene-in-the-pdf/
description: Aspose 的场景类。3D API 表示 3D 场景。开发人员可以通过添加相机，灯光，多边形和各种其他实体来构建 3D 场景。他们现在还可以将 3D 场景保存为 PDF 文件格式。
---
##  **概述**

本文介绍如何使用 C# .NET 3D 文件操作和转换 API 将 3D 文件转换为 PDF 格式，首先需要 [将 3D 文件加载到场景对象中](https://docs.aspose.com/3d/net/create-and-read-an-existing-3d-scene/)，然后将其保存为 PDF 格式。它涵盖了广泛的主题，例如

- 在 C# 中将 3D 转换为 PDF
- 在 C# 中将 FBX 转换为 PDF
- 在 C# 中将 STL 转换为 PDF
- 在 C# 中将 U3D 转换为 PDF
- 在 C# 中将 OBJ 转换为 PDF

{{% alert color="primary" %}} 

Aspose.3D API 的 [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) 类表示 3D 场景。开发人员可以通过添加相机，灯光，多边形和各种其他实体来构建 3D 场景。他们现在还可以将 3D 场景保存为 PDF 文件格式。

{{% /alert %}} {{% alert color="primary" %}} 

Aspose.3D for .NET 直接将 API 和版本号的信息写入输出文档。例如，在将绘图渲染到 PDF 时，Aspose.3D for .NET 将用值 “Aspose.3D” 填充 `Application` 字段，用值填充 `PDF Producer` 字段，例如 “Aspose.3D 17.9”。

请注意，您不能指示 Aspose.3D for .NET API 从输出文档中更改或删除此信息。

{{% /alert %}} 
##  **创建带有圆柱体的 3D PDF，并使用 CAD 优化的照明以阴影插图模式渲染**
`Scene` 类的Save方法允许以 PDF 格式保存 3D 场景。开发人员可以加载任何 3D 支持的文件或构建新的 3D 场景，他们可以以 PDF 格式保存 3D 场景，如以下 C# 代码示例所示:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET

            // Create a new scene
            Scene scene = new Scene();
            // Create a cylinder child node
            scene.RootNode.CreateChildNode("cylinder", new Cylinder()).Material = new PhongMaterial() { DiffuseColor = new Vector3(Color.DarkCyan) };
            // Set rendering mode and lighting scheme
            PdfSaveOptions opt = new PdfSaveOptions();
            opt.LightingScheme = PdfLightingScheme.CAD;
            opt.RenderMode = PdfRenderMode.ShadedIllustration;
            // Save in the PDF format
            scene.Save("output_out.pdf", opt);

{{< /highlight >}}
