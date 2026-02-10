---
title: 处理水印
type: docs
weight: 160
url: /zh/net/working-with-watermark/
---

{{% alert color="primary" %}} 

使用 Aspose.3D for .NET API，开发人员可以轻松地为 3D 文件添加盲水印，同时以任何支持的输出文件格式保存。

{{% /alert %}} 
# **创建 3D 场景**
首先，您需要从 3D 文件创建 3D 场景。以下代码片段展示了如何使用此功能：

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
string file = "template.3ds";
Scene scene = Scene.FromFile(file);
{{< /highlight >}}

# **编码水印**
Aspose.3D for .NET 通过 ``EncodeWatermark`` 方法向 3D 文件添加水印文本信息和水印密码。以下代码片段展示了如何使用此功能：

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
var numMeshes = 0;
scene.RootNode.Accept((Node node) =>
{
    var mesh = node.GetEntity<Mesh>();
    if (mesh != null)
    {
        numMeshes++;
        mesh = Watermark.EncodeWatermark(mesh, "HelloWorld", "1234");
        if (mesh != null)
        {
            node.Entity = mesh;
        }
    }
    return true;
});
{{< /highlight >}}

# **保存文档**
您可以保存到您想要的任何 3D 文件格式。以下代码片段展示了如何使用此功能：

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
string output = "output.fbx";
scene.Save(output, FileFormat.FBX7400ASCII);
{{< /highlight >}}