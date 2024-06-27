---
title: Düğüm hiyerarşisini ekleyin ve 3D sahnesinin birden fazla düğümleri arasında örgü geometrik verilerini paylaşın
type: docs
weight: 20
url: /tr/java/add-node-hierarchy-and-share-geometric-data-of-mesh-among-multiple-nodes-of-3d-scene/
description: Aspose.3D for Java has support of building a hierarchy of Nodes. The Node is basic building block of 3D scene and a hierarchy of nodes defines the logical structure of 3D scene, and provide visible content by attaching geometries, lights, and cameras to nodes.
---
##  **Düğüm hiyerarşisini 3D sahne belgesine ekleyin**
Aspose.3D for Java has support of building a hierarchy of Nodes. The `Node` is basic building block of 3D scene and a hierarchy of nodes defines the logical structure of 3D scene, and provide visible content by attaching geometries, lights, and cameras to nodes.
###  **Cene cene Graph ample xample**

Aspose.3D, her bir `Node` örneği birden fazla çocuk düğümüne sahip olabilir, bu örnekte, kök düğümünü döndürürsek, tüm çocuk düğümleri de etkilenir:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-AddNodeHierarchy.java" >}}
##  **Hare hare Mesh eoeometry ata ata ultiultiple Nodes arasında**
In order to diminish memory necessities, a single instance of `Mesh` Class can be bound to various instances of `Node` Class. Envision that you require a system where all 3D cubes seemed to be indistinguishable, however you required numerous a large number of them. You could spare memory by making one Mesh object when the system begins up. At that point, each time you required another shape, you make another Node object, then point that node to the one `Mesh`. This is called instancing. Aspose.3D for Java APIs allow to do instancing.
###  **Instancing örneği**
Rts (gerçek zamanlı strateji) oyunlarında, her zaman aynı 3D modeliyle birden fazla npcs (oyuncu olmayan karakter) görebiliriz, belki farklı renklerde, işleme motoru genellikle farklı npc'lerde aynı örgü geometri verilerini paylaşır, bu tekniğe anında denir.

{{% alert color="primary" %}} 

The `Mesh` class object is being used in the code. We can [create a Mesh class object as narrated there](https://docs.dynabic.com/display/3djava/Create+3D+Mesh+and+Scene).

{{% /alert %}} 

Örnek kodun stration emonstration:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-ShareMeshGeometryData.java" >}}


In bu örnek biz 3 küp düğümleri aynı örgü paylaşmak, her biri farklı renklerde farklı malzeme var.
