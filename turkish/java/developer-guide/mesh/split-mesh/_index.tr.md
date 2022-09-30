---
title: Split Mesh
type: docs
weight: 10
url: /tr/java/split-mesh/
description: Aspose.3D for Java API, bir sahnenin tüm kafeslerini malzeme başına birkaç alt kafese bölmeyi desteklemektedir. The pliplit. esh yöntemi, tek bir malzemeye atanmışsa, sahnenin bir ağını bölmez. It Aspose.3D 076. 481 076481 481 kullanarak elde edilebilir.
---
## **Cene plit cene cene er erial aterial tüm shes eshes**
Aspose.3D for Java API, bir sahnenin tüm kafeslerini malzeme başına birkaç alt kafese bölmeyi desteklemektedir. The pliplit. esh yöntemi, tek bir malzemeye atanmışsa, sahnenin bir ağını bölmez. It Aspose.3D 076. 481 076481 481 kullanarak elde edilebilir.

{{% alert color="primary" %}} 

`SplitMeshPolicy` enum, ağ bölme algoritmasında kullanılan veri politikasını belirtir, iki politikayı destekler, alt ağlar veya her bir alt ağ arasındaki verileri paylaşır (sadece kullanılan veriler).

{{% /alert %}} 

The kod örneği aşağıda malzeme başına bir sahnenin tüm ağlarını böler. Each alt ağ aynı doğrudan verileri paylaşır ve sadece endekslerde farklılık gösterir.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-mesh-SplitAllMeshesofScenebyMaterial.java" >}}
## **Erial plit a erial esh erial pecicithe erial aterial**
Aspose.3D for Java API, malzemeyi manuel olarak belirterek bir ağı bölmeyi desteklemektedir. The split mesh seçeneği ayrı nesneler oluşturur ve her alt örgü sadece bir malzeme kullanır.
### **Box Split Mesh**
Tonun yardım konusu kodu kapsamlı ve kısa tutmak için kutunun bir örgü oluşturur. Developers, bu yardım konusu olarak manuel olarak bir örgü oluşturabilir:[Create a 3D Cube Mesh](https://docs.dynabic.com/display/3djava/Create+3D+Mesh+and+Scene). Furthermore, bir kutu 6 uçak ile oluşur ve her uçak bir alt ağ haline gelir. The kod örneği aşağıda elle malzeme belirterek bir ilkel örgü böler.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-mesh-SplitMeshbyMaterial.java" >}}
