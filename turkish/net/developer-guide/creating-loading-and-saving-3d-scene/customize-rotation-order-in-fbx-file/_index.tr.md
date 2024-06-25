---
title: Rotationorder FBX dosyasında özelleştirin
type: docs
weight: 10
url: /tr/net/customize-rotation-order-in-fbx-file
description: Aspose.3D for .NET kullanarak, geliştiriciler rotationorder gibi yerel FBX özelliklerini özelleştirebilir.
---
{{% alert color="primary" %}}

Using [Aspose.3D for .NET](https://products.aspose.com/3d/net/), Sometimes, developers require fine control over format-specific features, such as changing the `RotationOrder` in the FBX exporter. While there might not be a public API directly exposing this functionality, Aspose.3D for .NET provides ways to achieve such customizations through its flexible architecture.
{{% /alert %}}



İşte bunu Aspose ile nasıl halledebilirsiniz? 3D:

{{% highlight "csharp" %}}

var rvm = Scene.FromFile(@"F1234.rvm");
rvm.RootNode.Accept((Node node) =>
{
    node.SetProperty("RotationOrder", 1); //set a custom property, exporter will match this to FBX's property.
    return true; //continue to traverse on other nodes 
});

rvm.Save(@"test.fbx");

{{% /highlight %}}

Bu örnekte:

1. RVM dosyasından bir sahne oluşturun.
1. Olay yerindeki tüm düğümleri ziyaret edin.
1.   Set custom property: The SetProperty method is used to set the `RotationOrder` property, demonstrating how internal mechanisms can be leveraged to control format-specific features not directly exposed by the public API.
1. Sahneyi kaydet: sahne özelleştirilmiş `RotationOrder` ile kaydedilir.

By using such techniques, Aspose.3D allows developers to fine-tune and control specific features of 3D formats, ensuring that detailed and precise requirements are met in various 3D applications.