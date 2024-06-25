---
title: Animasyon özelliği ve kurulum hedef kamerayı 3D belgesine ekleyin
type: docs
weight: 10
url: /tr/net/add-animation-property-and-setup-target-camera-in-3d-document/
description: Aspose.3D, nesne animasyonu aslında özellikler üzerinde animasyonlar yapan anahtar çerçeve animasyonudur. Özellikleri canlandırmak için, bir mülkün bileşenlerini farklı eğrilere eşleştiren bir eğrileme örneğine ihtiyacınız vardır, örneğin, bir vector3 özelliği, üç kanalı eğrilemede kuracak 3 bileşen x/y/z'ye sahip olabilir, her kanal bir eğri kümesine sahip olabilir.
---
##  **Animasyon özelliğini 3D belgesine ekleyin**
Aspose.3D for .NET animasyonlu sahne oluşturmayı destekler. Bu makale, bir nesneyi taşımak için ön şartları açıklar.
###  **Move Cube's Position**
{{% alert color="primary" %}}

The [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) class object is being used in the code. We can [create a Mesh class object as narrated there](/3d/net/create-and-read-an-existing-3d-scene/) and it's must animate the local translation property of the node too: [Adding the Transformation to the Node](/3d/net/adding-transformation-to-the-node/).

{{% /alert %}}

In Aspose.3D, object animation is actually key-frame animation that animates on properties. To animate properties, you need a `CurveMapping` instance which maps components of a property to different curves, for example, a `Vector3` property can have 3 components `X`/`Y`/`Z`, which will set up three channels in `CurveMapping`, every channel can have a set of `Curve`.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Animation-PropertyToDocument-AddAnimationPropertyToDocument.cs" >}}
##  **Hedef kamerayı 3D dosyasında kur**
Aspose.3D for .NET offers to setup the target camera in 3D file. In some file formats, light/camera supports target, which allows the light/camera always facing a specified node, this is useful in animation.

{{% alert color="primary" %}}

[`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene), [`Camera`](https://reference.aspose.com/3d/net/aspose.threed.entities/camera), [`Node`](https://reference.aspose.com/3d/net/aspose.threed/node) ve [`Transform`](https://reference.aspose.com/3d/net/aspose.threed/transform) sınıfları kodda kullanılıyor. `Scene`, [`Scene.Save`](https://reference.aspose.com/3d/net/aspose.threed/scene/methods/save) yöntemini kaydetmek için, tam yol ve [`FileFormat`](https://reference.aspose.com/3d/net/aspose.threed/fileformat) parametresi olan bir dosya adını kabul eder.

{{% /alert %}}

Aşağıdaki örnekte, hedef ve kamera 3D dosyasında kurulur:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Animation-SetupTargetAndCamera-SetupTargetAndCamera.cs" >}}
