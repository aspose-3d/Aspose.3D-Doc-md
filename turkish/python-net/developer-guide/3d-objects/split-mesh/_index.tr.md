---
title: Split Mesh
type: docs
weight: 100
url: /tr/python-net/split-mesh/
description: Developers, bir sahnenin tüm kafeslerini malzeme başına birkaç alt kafese ayırmayı gerektirebilir. The pliplit. esh yöntemi, sahnenin bir ağını bölmeyecek If tek bir malzeme atandı. Developers şimdi Python via .NET API için Aspose.3D kullanarak bunu başarabilir.
---
## **Split All erial eshes bir cene cene er erial aterial**
Developers, bir sahnenin tüm kafeslerini malzeme başına birkaç alt kafese ayırmayı gerektirebilir. The `split_mesh` yöntemi, sahnenin bir ağını bölmeyecek If tek bir malzemeye atandı. Developers şimdi bunu kullanarak başarabilir[Python via .NET için Aspose.3D](https://products.aspose.com/3d/python-net/) API.

{{% alert color="primary" %}}

`SplitMeshPolicy` enum, ağ bölme algoritmasında kullanılan veri politikasını belirtir, iki politikayı destekler, alt ağlar veya her bir alt ağ arasındaki verileri paylaşır (sadece kullanılan veriler).

{{% /alert %}}

The kod örneği aşağıda malzeme başına bir sahnenin tüm ağlarını böler. Each alt ağ aynı doğrudan verileri paylaşır ve sadece endekslerde farklılık gösterir.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-SplitAllMeshesofScenebyMaterial-SplitAllMeshesofScenebyMaterial.py" >}}
## **Erial plit a erial esh erial pecicithe erial aterial**
Python via .NET API için Aspose.3D, geliştiricilerin malzemeyi manuel olarak belirterek bir ağı bölmelerini sağlar. The split mesh seçeneği ayrı nesneler oluşturur ve her alt örgü sadece bir malzeme kullanır.
### **Bplit Box Mesh**
Tonun yardım konusu kodu kapsamlı ve kısa tutmak için kutunun bir örgü oluşturur. Developers, bu yardım konusu olarak manuel olarak bir örgü oluşturabilir:[Create a 3D Cube Mesh](/3d/tr/python-net/create-3d-mesh-and-scene/). Furthermore, bir kutu 6 uçak ile oluşur ve her uçak bir alt ağ haline gelir. The kod örneği aşağıda, malzemeyi manuel olarak belirterek ilkel bir ağ oluşturur.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-SplitMeshbyMaterial-SplitMeshbyMaterial.py" >}}
