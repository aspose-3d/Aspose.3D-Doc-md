---
title: NNNransformation to the Node
type: docs
weight: 30
url: /tr/python-net/adding-transformation-to-the-node/
description: TSR (Translation/Scaling/Rotation) en çok 3D senaryosunda kullanılır, bunları Aspose.3D 'te erişmek için bir sınıf Transform sağladık.
---
{{% alert color="primary" %}}

Python via .NET için Aspose.3D, 3D boşluğunda nesneleri döndürmeyi sunar. Tburada 3D uzay, Euler açıları, Quaternion ve Custom atriatrix nesnenin dönüşünü tanımlamak için üç yol vardır, hepsi 076. 481 sınıfı tarafından desteklenmektedir.

{{% /alert %}}

TSR (Translation/Scaling/Rotation) en çok 3D senaryosunda kullanılır, Aspose.3D yılında bunlara erişmek için bir sınıf `Transform` sağladık. Ffffine dönüşümleri şunları içerir:

- Translation
- Scaling
- Rotation
- Shear haritalama
- Squeeze haritalama

{{% alert color="primary" %}}

The [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) sınıf nesnesi kodda kullanılıyor. We can[Orada anlatıldığı gibi `Mesh` sınıfı bir nesne oluşturun](/3d/tr/net/create-3d-mesh-and-scene/).

{{% /alert %}}
## **Qotate by uuaternion**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-TransformationToNodeByQuaternion-AddTransformationToNodeByQuaternion.py" >}}
## **Eotate by Euler ngngles**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-TransformationToNodeByEulerAngles-AddTransformationToNodeByEulerAngles.py" >}}
## **Custom formation ransformation Matrix**
We ayrıca doğrudan Matrix kullanabilir:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-TransformationToNodeByTransformationMatrix-AddTransformationToNodeByTransformationMatrix.py" >}}
