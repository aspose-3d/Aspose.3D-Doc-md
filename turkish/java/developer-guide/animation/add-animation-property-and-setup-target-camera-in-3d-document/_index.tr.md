---
title: Add Animation roroperty ve Setup 07arget 07amera 3D belgesinde
type: docs
weight: 10
url: /tr/java/add-animation-property-and-setup-target-camera-in-3d-document/
description: Aspose.3D for Java animasyonlu sahne render destekler. This makalesi bir nesneyi hareket ettirmek için ön şartları açıklar.
---
## **Add Animation özelliği 3D belgesinde**
Aspose.3D for Java animasyonlu sahne render destekler. This makalesi bir nesneyi hareket ettirmek için ön şartları açıklar.
### **Move Cube's Position**
{{% alert color="primary" %}}

The `Mesh` sınıf nesnesi kodda kullanılıyor. We can[Orada anlatılan Mesh sınıfı bir nesne oluşturun](https://docs.aspose.com/3d/java/create-3d-mesh-and-scene/)Ve düğümün yerel çeviri özelliğini de canlandırmalıdır:[Tranransformation Node](https://docs.aspose.com/3d/java/adding-transformation-to-the-node/).

{{% /alert %}}

Animation n Aspose.3D for Java API, animasyon örneği aslında özellikler üzerinde animasyonlar yapan anahtar çerçeve animasyonudur. In sipariş animate özellikleri, bir mülkün bileşenlerini farklı eğrilere eşleştiren bir `CurveMapping` örneğine ihtiyacınız var, örneğin 076. 481 özelliği 3 bileşen 076481 481/`Y`/`Z`, 07three 3481 'de üç kanal kuracak, her kanal `Curve` bir dizi olabilir.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-animation-PropertyToDocument-AddAnimationPropertyToDocument.java" >}}
## **Setup 3D yılında Target Camera ile**
Aspose.3D for Java, hedef kamerayı 3D dosyasında kurmayı teklif eder. In bazı dosya biçimleri, ışık/kamera, ışık/kameranın her zaman belirtilen bir düğüme bakmasını sağlayan hedefi destekler, bu animasyonda yararlıdır.

{{% alert color="primary" %}}

The `Scene`, `Camera`, `Node` ve `Transform` sınıfları kodda kullanılıyor. 076481 481, 076. 481 yöntemini kaydetmek için, tam yol ve `FileFormat` parametresi olan bir dosya adını kabul eder.

{{% /alert %}}

In aşağıdaki örnekte, hedef ve kamera 3D dosyasında kurulur:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-animation-SetupTargetAndCamera.java" >}}
