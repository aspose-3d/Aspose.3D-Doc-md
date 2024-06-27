---
title: Animasyon özelliği ve kurulum hedef kamerayı 3D belgesine ekleyin
type: docs
weight: 10
url: /tr/java/add-animation-property-and-setup-target-camera-in-3d-document/
description: Aspose.3D for Java animasyonlu sahne oluşturmayı destekler. Bu makale, bir nesneyi taşımak için ön şartları açıklar.
---
##  **Animasyon özelliğini 3D belgesine ekleyin**
Aspose.3D for Java animasyonlu sahne oluşturmayı destekler. Bu makale, bir nesneyi taşımak için ön şartları açıklar.
###  **Move Cube's Position**
{{% alert color="primary" %}}

The `Mesh` class object is being used in the code. We can [create a Mesh class object as narrated there](https://docs.aspose.com/3d/java/create-3d-mesh-and-scene/) and it's must animate the local translation property of the node too: [Adding the Transformation to the Node](https://docs.aspose.com/3d/java/adding-transformation-to-the-node/).

{{% /alert %}}

In Aspose.3D for Java API, animation instance is actually key-frame animation that animates on properties. In order animate properties, you need a `CurveMapping` instance which maps components of a property to different curves, for example, a `Vector3` property can have 3 components `X`/`Y`/`Z`, which will set up three channels in `CurveMapping`, every channel can have a set of `Curve`.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-animation-PropertyToDocument-AddAnimationPropertyToDocument.java" >}}
##  **Hedef kamerayı 3D dosyasında kur**
Aspose.3D for Java offers to setup the target camera in 3D file. In some file formats, light/camera supports target, which allows the light/camera always facing a specified node, this is useful in animation.

{{% alert color="primary" %}}

`Scene`, `Camera`, `Node` ve `Transform` sınıfları kodda kullanılıyor. `Scene`, `Scene.save` yöntemini kaydetmek için, tam yol ve `FileFormat` parametresi ile bir dosya adını kabul eder.

{{% /alert %}}

Aşağıdaki örnekte, hedef ve kamera 3D dosyasında kurulur:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-animation-SetupTargetAndCamera.java" >}}
