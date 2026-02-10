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

{{< highlight "python" >}}
import aspose.threed as a3d
# For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
# The path to the documents directory.
# Create an object of the Scene class
scene = a3d.Scene()
# Save 3D scene document
scene.Save("document.fbx", a3d.FileFormat.FBX7500ASCII)

{{< /highlight >}}

### **Mevcut Bir Dosya Nasıl Açılır?**

Aşağıdaki örnek, "document.fbx" adlı mevcut bir 3D şablon dosyasını açar.

{{< highlight "python" >}}
import aspose.threed as a3d
# For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
# The path to the documents directory.

# Initialize a Scene class object
scene = Scene()
# Load an existing 3D document
scene.open("document.fbx")


{{< /highlight >}}
