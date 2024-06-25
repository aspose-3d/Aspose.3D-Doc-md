---
title: 从 C# 中的 PDF 导入 3D 场景和内容
linktitle: 从 PDF 导入 3D 场景和内容
type: docs
weight: 50
url: /zh/net/import-3d-scenes-and-contents-from-a-pdf/
keywords: 3d pdf, 3d pdf c#
description: Aspose 的场景类。3D API 表示 3D 场景。开发人员可以从 PDF 文件中提取 3D 场景和内容。
---
{{% alert color="primary" %}}

Aspose.3D API 的 [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) 类表示 3D 场景。开发人员可以从 PDF 文件中提取 3D 场景和内容。

{{% /alert %}}
##  **从受密码保护的 PDF 打开场景**
`Scene` 类的 `Open` 方法允许从输入 PDF 文件加载 3D 场景。开发人员还可以使用 [`PdfLoadOptions`](https://reference.aspose.com/3d/net/aspose.threed.formats/pdfloadoptions) 类为受保护的pdf应用密码，如以下 C# 代码示例所示:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-OpenSceneFromProtectedPdf-OpenSceneFromProtectedPdf.cs" >}}
##  **从 PDF 中提取所有原始 3D 内容**
[`PdfFormat`](https://reference.aspose.com/3d/net/aspose.threed.formats/pdfformat) 类的Extract方法允许从 PDF 文件中提取 3D 内容。开发人员可以遍历内容，并将它们保存到单独的文件中，如 C# 代码示例所示:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-ExtractRaw3DContentsFromPdf-ExtractRaw3DContentsFromPdf.cs" >}}
##  **提取所有 3D 场景并将其保存为支持的 3D 格式**
`PdfFormat` 类的 `ExtractScene` 方法允许从 PDF 文件中提取 3D 场景。开发人员可以遍历场景，并将它们保存为支持的 3D 文件格式，如以下 C# 代码示例所示:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-ExtractAll3DScenes-ExtractAll3DScenes.cs" >}}

{{% alert color="primary" %}}

所有受支持的 3D 文件格式都列在 [产品概述](/3d/zh/net/product-overview/) 页中。

{{% /alert %}}
