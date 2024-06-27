---
title: Export texture files while saving 3D scene
type: docs
weight: 10
url: /tr/net/export-texture-files-while-saving-3d-scene
description: Aspose.3D for .NET kullanarak, geliştiriciler doku dosyalarını dosya sistemine ihraç ederken 3D görüntüsünü kaydedebilir.
---
{{% alert color="primary" %}}

[Aspose.3D for .NET](https://products.aspose.com/3d/net/) kullanarak, bir sahneyi dosyalara aktarırken, dokuları gömülü veya harici olarak aynı dizine ihraç etmek genellikle gereklidir. Aspose.3D for .NET bu süreci kolaylaştırır, tüm dokuların düzgün bir şekilde yönetilmesini ve ihraç edilen sahne ile birlikte saklanmasını sağlar. Bu kılavuz bunu nasıl başaracağınızı gösterir.

{{% /alert %}}

Bir sahneyi dışa aktarmak ve tüm ilgili dokuların aynı dizine kaydedilmesini sağlamak için şu adımları izleyin:


{{% highlight "csharp" %}}

Scene scene = Scene.FromFile(@"BoomBox.glb");
var opt = new ObjSaveOptions();
opt.ExportTextures = true;
scene.Save(@"D:\tmp\boombox\output.obj", opt);

{{% /highlight %}}


Tüm `SaveOptions` nesneleri Aspose.3D, ihracat sırasında dokuları yönetme sürecini basitleştiren `ExportTextures` özelliğini içerir. Bu özellik, harici veya gömülü olsun, tüm dokuların belirtilen çıkış dizinine kaydedilmesini sağlar. Bu özellik, FBX, 3DS, OBJ, USD, GLTF ve DAE gibi doku ihracatını destekleyen çeşitli dosya formatlarıyla uyumludur.



Açıklama

1. Sahneyi yükle: sahne giriş dosyasından yüklenir.
1.  Configure Save Options: Set `ExportTextures` to `true`.
1. Sahneyi dışa aktarın: sahne güncellenmiş doku yolları ile çıkış dizinine kaydedilir.


`ExportTextures` özelliğini `SaveOptions` olarak kullanarak, tüm gerekli varlıkların tek bir dizinde düzenlenmesini sağlayarak, dokularıyla birlikte 3D sahnelerini sorunsuz bir şekilde dışa aktarabilirsiniz. Bu özellik, çeşitli platformlar ve uygulamalar arasında 3D dosyalarının taşınabilirliğini ve kullanım kolaylığını artırır.

##  **Resources**

1. [Çevrimiçi öğretici](https://products.aspose.com/3d/tutorial/)
1. [Seçenekler](https://reference.aspose.com/3d/net/aspose.threed.formats/saveoptions/)
