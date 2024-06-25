---
title: Düğüm hiyerarşisini ekleyin ve 3D sahnesinin birden fazla düğümleri arasında örgü geometrik verilerini paylaşın
type: docs
weight: 40
url: /tr/python-net/add-node-hierarchy-and-share-geometric-data-of-mesh-among-multiple-nodes-of-3d-scene/
description: Aspose.3D for Python via .NET bir düğüm hiyerarşisi oluşturmayı teklif eder. Düğüm, bir sahnenin temel yapı bloğudur. Düğümlerin bir hiyerarşi, bir sahnenin mantıksal yapısını tanımlar ve geometrileri, ışıkları ve kameraları düğümlere bağlayarak görünür içerik sağlar.
---
##  **Düğüm hiyerarşisini 3D sahne belgesine ekleyin**
Aspose.3D for Python via .NET bir düğüm hiyerarşisi oluşturmayı teklif eder. Düğüm, bir sahnenin temel yapı bloğudur. Düğümlerin bir hiyerarşi, bir sahnenin mantıksal yapısını tanımlar ve geometrileri, ışıkları ve kameraları düğümlere bağlayarak görünür içerik sağlar.
###  **Cene cene Graph ample xample**
A örnek sahne hiyerarşi gibi görünüyor:

! [Todo: image_alt_text](add-node-hierarchy-and-share-geometric-data-of-mesh-among-multiple-nodes-of-3d-scene_1.png)

Aspose.3D, her bir `Node` örneği birden fazla çocuk düğümüne sahip olabilir, bu örnekte, kök düğümünü döndürürsek, tüm çocuk düğümleri de etkilenir:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-NodeHierarchy-AddNodeHierarchy.py" >}}
##  **Hare hare Mesh eoeometry ata ata ultiultiple Nodes arasında**
To diminish memory necessities, a single instance of [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) Class can be bound to various instances of [`Node`](https://reference.aspose.com/3d/net/aspose.threed/node) Class. Envision that you require a system where all 3D cubes seemed to be indistinguishable, however you required numerous a large number of them. You could spare memory by making one Mesh object when the system begins up. At that point, each time you required another shape, you make another Node object, then point that node to the one Mesh. This is called instancing. Aspose.3D for Python via .NET APIs allow to do instancing.
###  **Instancing örneği**
Rts (gerçek zamanlı strateji) oyunlarında, her zaman aynı 3D modeliyle birden fazla npcs (oyuncu olmayan karakter) görebiliriz, belki farklı renklerde, işleme motoru genellikle farklı npc'lerde aynı örgü geometri verilerini paylaşır, bu tekniğe anında denir.

{{% alert color="primary" %}}

The `Mesh` class object is being used in the code. We can [create a `Mesh` class object as narrated there](/3d/python-net/create-3d-mesh-and-scene/).

{{% /alert %}}

Örnek kodun stration emonstration:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Geometry-and-Hierarchy-MeshGeometryData-ShareMeshGeometryData.py" >}}

In bu örnek biz 3 küp düğümleri aynı örgü paylaşmak, her biri farklı renklerde farklı malzeme var.
