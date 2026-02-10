---
title: 在 PDF 中保存 3D 场景
type: docs
weight: 60
url: /zh/python-net/save-a-3d-scene-in-the-pdf/
description: Aspose 的场景类。3D API 表示 3D 场景。开发人员可以通过添加相机，灯光，多边形和各种其他实体来构建 3D 场景。他们现在还可以将 3D 场景保存为 PDF 文件格式。
---
{{% alert color="primary" %}} 

Aspose.3D API 的 [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) 类表示 3D 场景。开发人员可以通过添加相机，灯光，多边形和各种其他实体来构建 3D 场景。他们现在还可以将 3D 场景保存为 PDF 文件格式。

{{% /alert %}} {{% alert color="primary" %}} 

Aspose.3D for Python via .NET 直接将 API 和版本号的信息写入输出文档。例如，在将绘图渲染到 PDF 时，Aspose.3D for Python via .NET 会使用值 “Aspose.3D” 填充 `Application` 字段，并使用值填充 `PDF Producer` 字段，例如 “Aspose.3D 17.9”。

请注意，您不能指示 Python via .NET API 的 Aspose.Diagram从输出文档中更改或删除此信息。

{{% /alert %}} 
##  **创建带有圆柱体的 3D PDF，并使用 CAD 优化的照明以阴影插图模式渲染**
`Scene` 类的Save方法允许以 PDF 格式保存 3D 场景。开发人员可以加载任何 3D 支持的文件或构建新的 3D 场景，他们可以将 3D 场景保存为 PDF 格式，如下面的代码示例所示:

{{< highlight "python" >}}
from aspose.threed import Scene
from aspose.threed.entities import Cylinder
from aspose.threed.shading import PhongMaterial
from aspose.threed.formats import PdfSaveOptions, PdfLightingScheme, PdfRenderMode
# Create a new scene
scene = Scene()
# Create a cylinder child node
cylinder = scene.root_node.create_child_node("cylinder", Cylinder())
cylinder.material = PhongMaterial()
# Set rendering mode and lighting scheme
opt = PdfSaveOptions()
opt.lighting_scheme = PdfLightingScheme.CAD
opt.render_mode = PdfRenderMode.SHADED_ILLUSTRATION
# Save in the PDF format
scene.save("output_out.pdf", opt)

{{< /highlight >}}
