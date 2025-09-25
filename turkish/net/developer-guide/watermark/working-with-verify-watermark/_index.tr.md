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

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-WorkingWithWatermark-Create3DScene.cs" >}}

# **Filigranı Çözme**
Aspose.3D for .NET, 3B dosyanın şifresini girdikten sonra filigranı doğrulamak için `DecodeWatermark` yöntemini kullanır. Aşağıdaki kod parçacığı bu işlevselliğin nasıl kullanılacağını göstermektedir:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-WorkingWithVerifyWatermark-DecodeWatermark.cs" >}}

# **Belge Onayı**
Dönen sonuç için, dönen sonuç null ise, bu, 3B belgeye filigran eklenmediği anlamına gelir. Metin bilgisi döndürürse, bu 3B dosyanın filigranıdır. Şifre yanlış girilirse, bir hata mesajı döndürülür.