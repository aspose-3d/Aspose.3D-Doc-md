---
title: Verify Sürdürme ile çalışma
type: docs
weight: 170
url: /tr/net/working-with-verify-watermark/
---

{{% alert color="primary" %}}

Aspose.3D for .NET API'si ile geliştiriciler, herhangi bir desteklenen çıktı dosya formatında kaydederken 3B dosyalara kör filigran doğrulaması ekleyebilirler.

{{% /alert %}}
# **3B Sahne Oluşturma**
İlk olarak, bir 3B dosyadan bir 3B sahne oluşturmanız gerekir. Aşağıdaki kod parçacığı bu işlevselliğin nasıl kullanılacağını göstermektedir:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
string file = "template.3ds";
Scene scene = Scene.FromFile(file);
{{< /highlight >}}

# **Filigranı Çözme**
Aspose.3D for .NET, 3B dosyanın şifresini girdikten sonra filigranı doğrulamak için `DecodeWatermark` yöntemini kullanır. Aşağıdaki kod parçacığı bu işlevselliğin nasıl kullanılacağını göstermektedir:

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
string text = null;
try
{
    scene.RootNode.Accept((Node node) =>
    {
        var mesh = node.GetEntity<Mesh>();
        if (mesh != null)
        {
            text = Watermark.DecodeWatermark(mesh, "1234");
            if (text != null)
                return false;
        }
        return true;
    });
}
catch (UnauthorizedAccessException)
{
    return "Password error";
}
return text;
{{< /highlight >}}

# **Belge Onayı**
Dönen sonuç için, dönen sonuç null ise, bu, 3B belgeye filigran eklenmediği anlamına gelir. Metin bilgisi döndürürse, bu 3B dosyanın filigranıdır. Şifre yanlış girilirse, bir hata mesajı döndürülür.