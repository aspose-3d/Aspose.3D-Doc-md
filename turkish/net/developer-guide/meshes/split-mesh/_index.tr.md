---
title: Split Mesh
type: docs
weight: 100
url: /tr/net/split-mesh/
description: Geliştiriciler, bir sahnenin tüm kafeslerini malzeme başına birkaç alt kafese ayırmayı gerektirebilir. Tek bir malzemeye atanmışsa, splitmesh yöntemi sahnenin bir ağını bölmez. Geliştiriciler şimdi Aspose kullanarak bunu başarabilirler. 3D for .NET API.
---
##  **Split All erial eshes bir cene cene er erial aterial**
Geliştiriciler, bir sahnenin tüm kafeslerini malzeme başına birkaç alt kafese ayırmayı gerektirebilir. Tek bir malzemeye atanmışsa, splitmesh yöntemi sahnenin bir ağını bölmez. Geliştiriciler şimdi [Aspose.3D for .NET](https://products.aspose.com/3d/net/) API kullanarak bunu başarabilirler.

{{% alert color="primary" %}}

`SplitMeshPolicy` enum, ağ bölme algoritmasında kullanılan veri politikasını belirtir, iki politikayı destekler, alt ağlar veya her bir alt ağ arasındaki verileri paylaşır (sadece kullanılan veriler).

{{% /alert %}}

The kod örneği aşağıda malzeme başına bir sahnenin tüm ağlarını böler. Each alt ağ aynı doğrudan verileri paylaşır ve sadece endekslerde farklılık gösterir.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Working-with-Objects-SplitAllMeshesofScenebyMaterial-SplitAllMeshesofScenebyMaterial.cs" >}}
##  **Erial plit a erial esh erial pecicithe erial aterial**
Aspose.3D for .NET API, geliştiricilerin malzemeyi manuel olarak belirterek bir ağı ayırmasına izin verir. Bölünmüş örgü seçeneği ayrı nesneler oluşturur ve her alt örgü sadece bir malzeme kullanır.
###  **Bplit Box Mesh**
Bu yardım konusu, kodu kapsamlı ve kısa tutmak için kutunun bir örgü oluşturur. Geliştiriciler, bu yardım konusu hakkında manuel olarak bir ağ oluşturabilirler: [3D küp mesh oluşturun](/3d/tr/net/create-3d-mesh-and-scene/). Ayrıca, bir kutu 6 uçak ile oluşur ve her uçak bir alt ağ haline gelir. Aşağıdaki kod örneği, malzemeyi manuel olarak belirterek ilkel bir ağ oluşturur.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Working-with-Objects-SplitMeshbyMaterial-SplitMeshbyMaterial.cs" >}}
