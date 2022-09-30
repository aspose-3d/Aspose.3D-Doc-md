---
title: NNNransformation to the Node
type: docs
weight: 30
url: /tr/net/adding-transformation-to-the-node/
description: TSR (Translation/Scaling/Rotation) en çok 3D senaryosunda kullanılır, bunları Aspose.3D 'te erişmek için bir sınıf Transform sağladık.
---
{{% alert color="primary" %}}

Aspose.3D for .NET, 3D alanındaki nesneleri döndürmeyi teklif eder. Tburada 3D uzay, Euler açıları, Quaternion ve Custom atriatrix nesnenin dönüşünü tanımlamak için üç yol vardır, hepsi 076. 481 sınıfı tarafından desteklenmektedir.

{{% /alert %}}

TSR (Translation/Scaling/Rotation) en çok 3D senaryosunda kullanılır, Aspose.3D yılında bunlara erişmek için bir sınıf `Transform` sağladık. Ffffine dönüşümleri şunları içerir:

- Translation
- Scaling
- Rotation
- Shear haritalama
- Squeeze haritalama

{{% alert color="primary" %}}

The [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) sınıf nesnesi kodda kullanılıyor. We can[Orada anlatılan Mesh sınıfı bir nesne oluşturun](/3d/tr/net/create-3d-mesh-and-scene/).

{{% /alert %}}
## **Qotate by uuaternion**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Geometry-and-Hierarchy-TransformationToNodeByQuaternion-AddTransformationToNodeByQuaternion.cs" >}}
## **Eotate by Euler ngngles**
{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Geometry-and-Hierarchy-TransformationToNodeByEulerAngles-AddTransformationToNodeByEulerAngles.cs" >}}
## **Custom formation ransformation Matrix**
We ayrıca doğrudan Matrix kullanabilir:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Geometry-and-Hierarchy-TransformationToNodeByTransformationMatrix-AddTransformationToNodeByTransformationMatrix.cs" >}}
