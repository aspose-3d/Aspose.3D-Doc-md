---
title: Add Node hiyerarşi ve Share eoeometrik veri 07esh arasında ultiultiple Nodes 3D cene cene
type: docs
weight: 40
url: /tr/net/add-node-hierarchy-and-share-geometric-data-of-mesh-among-multiple-nodes-of-3d-scene/
description: Aspose.3D for .NET bir Node hiyerarşi inşa etmeyi teklif ediyor. The Node, bir sahnenin temel yapı bloğudur. Düğümlerin hiyerarşi, bir sahnenin mantıksal yapısını tanımlar ve geometrileri, ışıkları ve kameraları düğümlere bağlayarak görünür içerik sağlar.
---
## **Add Node 07ierarchy 3D Scene ococument**
Aspose.3D for .NET bir Node hiyerarşi inşa etmeyi teklif ediyor. The Node, bir sahnenin temel yapı bloğudur. Düğümlerin hiyerarşi, bir sahnenin mantıksal yapısını tanımlar ve geometrileri, ışıkları ve kameraları düğümlere bağlayarak görünür içerik sağlar.
### **Cene cene Graph ample xample**
A örnek sahne hiyerarşi gibi görünüyor:

![Todo: görüntü_Alt_Metin](add-node-hierarchy-and-share-geometric-data-of-mesh-among-multiple-nodes-of-3d-scene_1.png)

In Aspose.3D, her `Node` örneği birden fazla çocuk düğümüne sahip olabilir, bu örnekte, kök düğümünü döndürürsek, tüm çocuk düğümleri de etkilenir:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Geometry-and-Hierarchy-NodeHierarchy-AddNodeHierarchy.cs" >}}
## **Hare hare Mesh eoeometry ata ata ultiultiple Nodes arasında**
To bellek gereksinimlerini azaltır, [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) Class tek bir örnek [`Node`](https://reference.aspose.com/3d/net/aspose.threed/node) lass lass çeşitli örneklerine bağlı olabilir. Envision, tüm 3D küplerinin ayırt edilemez göründüğü bir sisteme ihtiyacınız var, ancak çok sayıda çok sayıda ihtiyacınız vardı. You sistem başladığında bir Mesh nesnesi yaparak bellek ayırabilir. At bu nokta, her zaman başka bir şekle ihtiyacınız olduğunda, başka bir Node nesnesi yaparsınız, daha sonra bu düğümün bir Mesh. This instancing olarak adlandırılır. Aspose.3D 076. 481 APIs instancing yapmak için izin verir.
### **Instancing örneği**
In RTS (Real-time strategy) gibi oyunlar, biz her zaman aynı 3D modeli ile birden fazla NPCs (Non-Player layer haracter) görebilirsiniz, belki farklı renklerde, işleme motoru genellikle aynı örgü geometri verilerini farklı NCCs arasında paylaşır, bu teknik Instancing olarak adlandırılır.

{{% alert color="primary" %}}

The `Mesh` sınıf nesnesi kodda kullanılıyor. We can[Orada anlatılan Mesh sınıfı bir nesne oluşturun](/3d/tr/net/create-3d-mesh-and-scene/).

{{% /alert %}}

Örnek kodun stration emonstration:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Geometry-and-Hierarchy-MeshGeometryData-ShareMeshGeometryData.cs" >}}

In bu örnek biz 3 küp düğümleri aynı örgü paylaşmak, her biri farklı renklerde farklı malzeme var.
