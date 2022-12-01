---
title: NNNransformation to the Node
type: docs
weight: 10
url: /tr/java/adding-transformation-to-the-node/
description: Aspose.3D for Java API 3D uzayda nesneleri döndürme desteği vardır. Tburada 076. 481 uzay, Euler açıları, Quaternion ve Custom Matrix nesnelerin dönüşünü tanımlamak için üç yol vardır, hepsi Transform sınıfı tarafından desteklenmektedir.
---
{{% alert color="primary" %}} 

Aspose.3D for Java API 3D uzayda nesneleri döndürme desteği vardır. Tburada 076. 481 uzay, Euler açıları, Quaternion ve Custom atriatrix nesnelerin dönüşünü tanımlamak için üç yol vardır, hepsi 076. 481 sınıfı tarafından desteklenmektedir.

{{% /alert %}} 

TSR (Translation/Scaling/Rotation) en çok 3D senaryosunda kullanılır, Aspose.3D ffffine dönüşümlerinde bunlara erişmek için `Transform` sınıfı sağladık:

- Translation
- Scaling
- Rotation
- Shear haritalama
- Squeeze haritalama

{{% alert color="primary" %}} 

The `Mesh` sınıf nesnesi kodda kullanılıyor. We can[Orada anlatılan Mesh sınıfı bir nesne oluşturun](https://docs.dynabic.com/display/3djava/Create+3D+Mesh+and+Scene).

{{% /alert %}} 
## **Qotate by uuaternion**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-AddTransformationToNodeByQuaternion.java" >}}
## **Eotate by Euler ngngles**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-AddTransformationToNodeByEulerAngles.java" >}}
## **Custom formation ransformation Matrix**
We ayrıca doğrudan Matrix kullanabilir:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-AddTransformationToNodeByTransformationMatrix.java" >}}
