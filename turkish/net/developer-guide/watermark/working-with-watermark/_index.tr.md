---
title: Su İşareti ile Çalışma
type: docs
weight: 160
url: /tr/net/working-with-watermark/
---

{{% alert color="primary" %}}

Aspose.3D for .NET API'si ile geliştiriciler, herhangi bir desteklenen çıktı dosya biçiminde kaydederken 3B dosyalara görünmez filigran ekleyebilirler.

{{% /alert %}}
# **3B Sahne Oluşturma**
İlk olarak, bir 3B dosyadan bir 3B sahne oluşturmanız gerekir.Aşağıdaki kod parçacığı bu işlevselliğin nasıl kullanılacağını göstermektedir:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
string file = "template.3ds";
Scene scene = Scene.FromFile(file);
{{< /highlight >}}

# **Filigran Kodlama**
Aspose.3D for .NET, ``EncodeWatermark`` yöntemi aracılığıyla 3B dosyalara filigran metin bilgisi ve filigran parolası ekler. Aşağıdaki kod parçacığı bu işlevselliğin nasıl kullanılacağını göstermektedir:

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

# **Belge Kaydetme**
İstediğiniz herhangi bir 3B dosya biçimine kaydedebilirsiniz.Aşağıdaki kod parçacığı bu işlevselliğin nasıl kullanılacağını göstermektedir:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
string output = "output.fbx";
scene.Save(output, FileFormat.FBX7400ASCII);
{{< /highlight >}}