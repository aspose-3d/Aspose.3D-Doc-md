---
title: Add Animation roroperty ve Setup 07arget 07amera 3D belgesinde
type: docs
weight: 10
url: /tr/net/add-animation-property-and-setup-target-camera-in-3d-document/
description: In Aspose.3D, nesne animasyonu aslında özellikler üzerinde canlanan anahtar çerçeve animasyonudur. To animate özellikleri, bir mülkün bileşenlerini farklı eğrilere haritalandıran bir Curveaapping örneğine ihtiyacınız var, örneğin, bir Vector3 özelliği, üç kanal kuracak 3 bileşen X/Y/Z olabilir.
---
## **Add Animation özelliği 3D belgesinde**
Aspose.3D for .NET animasyonlu sahne render destekler. This makalesi bir nesneyi hareket ettirmek için ön şartları açıklar.
### **Move Cube's Position**
{{% alert color="primary" %}}

The [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) sınıf nesnesi kodda kullanılıyor. We can[Orada anlatılan Mesh sınıfı bir nesne oluşturun](/3d/tr/net/create-and-read-an-existing-3d-scene/)Ve düğümün yerel çeviri özelliğini de canlandırmalıdır:[Tranransformation Node](/3d/tr/net/adding-transformation-to-the-node/).

{{% /alert %}}

In Aspose.3D, nesne animasyonu aslında özellikler üzerinde canlanan anahtar çerçeve animasyonudur. To animate özellikleri, bir özelliğin bileşenlerini farklı eğrilere eşleştiren bir `CurveMapping` örneğine ihtiyacınız var, örneğin `Vector3` özelliği `X`/076. 481/076481 481, `CurveMapping` yılında üç kanal kuracak, her kanal `Curve` kümesine sahip olabilir.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Animation-PropertyToDocument-AddAnimationPropertyToDocument.cs" >}}
## **Setup 3D yılında Target Camera ile**
Aspose.3D for .NET, hedef kamerayı 3D dosyasında kurmayı teklif eder. In bazı dosya biçimleri, ışık/kamera, ışık/kameranın her zaman belirtilen bir düğüme bakmasını sağlayan hedefi destekler, bu animasyonda yararlıdır.

{{% alert color="primary" %}}

The [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene), [`Camera`](https://reference.aspose.com/3d/net/aspose.threed.entities/camera), [`Node`](https://reference.aspose.com/3d/net/aspose.threed/node) ve [`Transform`](https://reference.aspose.com/3d/net/aspose.threed/transform) sınıfları kodda kullanılıyor. To bir 076. 481, 076. 481 yöntemi kullanılıyor, tam yol ve [`FileFormat`](https://reference.aspose.com/3d/net/aspose.threed/fileformat) parametresi olan bir dosya adını kabul ediyor.

{{% /alert %}}

In aşağıdaki örnekte, hedef ve kamera 3D dosyasında kurulur:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Animation-SetupTargetAndCamera-SetupTargetAndCamera.cs" >}}
