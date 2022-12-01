---
title: 从C#中的PDF导入3D场景和内容
linktitle: 从PDF导入3D场景和内容
type: docs
weight: 50
url: /zh/net/import-3d-scenes-and-contents-from-a-pdf/
keywords: 3d pdf, 3d pdf c#
description: Aspose.3D API的场景类表示3D场景。开发人员可以从PDF文件中提取3D场景和内容。
---
{{% alert color="primary" %}}

Aspose.3D API的[`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene)类表示3D场景。开发人员可以从PDF文件中提取3D场景和内容。

{{% /alert %}}
## **从密码保护PDF打开场景**
`Scene`类的`Open`方法允许从输入PDF文件加载3D场景。开发人员还可以使用[`PdfLoadOptions`](https://reference.aspose.com/3d/net/aspose.threed.formats/pdfloadoptions)类为受保护的pdf应用密码，如C#代码示例所示:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-OpenSceneFromProtectedPdf-OpenSceneFromProtectedPdf.cs" >}}
## **从PDF中提取所有原始3D内容**
[`PdfFormat`](https://reference.aspose.com/3d/net/aspose.threed.formats/pdfformat)类的提取方法允许从PDF文件中提取3D内容。开发人员可以遍历内容，并将其保存到单独的文件中，如以下C#代码示例所示:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-ExtractRaw3DContentsFromPdf-ExtractRaw3DContentsFromPdf.cs" >}}
## **提取所有3D场景并将其保存为支持的3D格式**
`PdfFormat`类的`ExtractScene`方法允许从PDF文件中提取3D场景。开发人员可以遍历场景，并将其保存为支持的3D文件格式，如以下C#代码示例所示:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-ExtractAll3DScenes-ExtractAll3DScenes.cs" >}}

{{% alert color="primary" %}}

所有支持的3D文件格式都列在[产品概述](/3d/zh/net/product-overview/)页。

{{% /alert %}}
