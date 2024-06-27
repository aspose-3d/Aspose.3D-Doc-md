---
title: Split Mesh
type: docs
weight: 10
url: /tr/java/split-mesh/
description: Aspose.3D for Java API has support to split all meshes of a scene into several sub meshes per material. The SplitMesh method will not split a mesh of the scene, if it has been assigned a single material. It can be achieved by using Aspose.3D for Java API.
---
##  **Cene plit cene cene er erial aterial tüm shes eshes**
Aspose.3D for Java API has support to split all meshes of a scene into several sub meshes per material. The SplitMesh method will not split a mesh of the scene, if it has been assigned a single material. It can be achieved by using Aspose.3D for Java API.

{{% alert color="primary" %}} 

`SplitMeshPolicy` enum, ağ bölme algoritmasında kullanılan veri politikasını belirtir, iki politikayı destekler, alt ağlar veya her bir alt ağ arasındaki verileri paylaşır (sadece kullanılan veriler).

{{% /alert %}} 

The kod örneği aşağıda malzeme başına bir sahnenin tüm ağlarını böler. Each alt ağ aynı doğrudan verileri paylaşır ve sadece endekslerde farklılık gösterir.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-mesh-SplitAllMeshesofScenebyMaterial.java" >}}
##  **Erial plit a erial esh erial pecicithe erial aterial**
Aspose.3D for Java API malzemeyi manuel olarak belirterek bir ağı bölmeyi desteklemektedir. Bölünmüş örgü seçeneği ayrı nesneler oluşturur ve her alt örgü sadece bir malzeme kullanır.
###  **Box Split Mesh**
Bu yardım konusu, kodu kapsamlı ve kısa tutmak için kutunun bir örgü oluşturur. Geliştiriciler, bu yardım konusu hakkında manuel olarak bir ağ oluşturabilirler: [3D küp mesh oluşturun](https://docs.dynabic.com/display/3djava/Create+3D+Mesh+and+Scene). Ayrıca, bir kutu 6 uçak ile oluşur ve her uçak bir alt ağ haline gelir. Aşağıdaki kod örneği, malzemeyi manuel olarak belirterek ilkel bir ağ oluşturur.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-mesh-SplitMeshbyMaterial.java" >}}
