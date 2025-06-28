---
title: İlk Aspose.3D Uygulamanız
type: docs
weight: 30
url: /tr/python-net/your-first-aspose-3d-application/
---

{{% alert color="primary" %}}

Bu öğretici, Aspose.3D'in basit API'sini kullanarak ilk uygulamanızı oluşturma sürecini açıklar. Bu basit uygulama, belirtilen bir 3D sahnesinde bir 3D dosyası oluşturur.

{{% /alert %}}

## **Uygulama Nasıl Oluşturulur?**

Aşağıdaki adımlar Aspose.3D API kullanılarak uygulamayı oluşturur:

1. [Scene](https://reference.aspose.com/3d/tr/python-net/aspose.threed/scene/) sınıfının bir örneğini oluşturun.
1. Bir lisansınız varsa bunu [uygulayın](/3d/tr/python-net/licensing/).
   Değerlendirme sürümünü kullanıyorsanız, lisansla ilgili kod satırlarını atlayın.
1. Yeni bir 3D dosyası oluşturun veya mevcut bir 3D dosyasını açın.
1. 3D dosyasındaki sahne içeriğine erişin.
1. Değiştirilen 3D dosyasını oluşturun.

Yukarıdaki adımların uygulanışı aşağıdaki örneklerde gösterilmiştir.

### **Yeni Bir Sahne Belgesi Nasıl Oluşturulur?**

Aşağıdaki örnek, sıfırdan yeni bir 3D sahne dosyası oluşturur. İlk olarak bir 3D sahnesi oluşturun ve ardından dosyayı FBX formatında kaydedin.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-CreateEmpty3DDocument.py" >}}

### **Mevcut Bir Dosya Nasıl Açılır?**

Aşağıdaki örnek, "document.fbx" adlı mevcut bir 3D şablon dosyasını açar.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-ReadExistingScene.py" >}}
