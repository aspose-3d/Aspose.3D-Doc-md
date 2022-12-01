---
title: Add Node hiyerarşi ve Share eoeometrik veri 07esh arasında ultiultiple Nodes 3D cene cene
type: docs
weight: 20
url: /tr/java/add-node-hierarchy-and-share-geometric-data-of-mesh-among-multiple-nodes-of-3d-scene/
description: Aspose.3D for Java, Nodes hiyerarşisini oluşturmayı desteklemektedir. The Node, 3D sahnesinin temel yapı bloğudur ve düğümlerin bir hiyerarşi 3D sahnesinin mantıksal yapısını tanımlar ve geometrileri, ışıkları ve kameraları düğümlere bağlayarak görünür içerik sağlar.
---
## **Add Node 07ierarchy 3D Scene ococument**
Aspose.3D for Java, Nodes hiyerarşisini oluşturmayı desteklemektedir. The `Node`, 3D sahnesinin temel yapı bloğudur ve düğümlerin hiyerarşi 076. 481 sahnesinin mantıksal yapısını tanımlar ve geometrileri, ışıkları ve kameraları düğümlere bağlayarak görünür içerik sağlar.
### **Cene cene Graph ample xample**

In Aspose.3D, her `Node` örneği birden fazla çocuk düğümüne sahip olabilir, bu örnekte, kök düğümünü döndürürsek, tüm çocuk düğümleri de etkilenir:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-AddNodeHierarchy.java" >}}
## **Hare hare Mesh eoeometry ata ata ultiultiple Nodes arasında**
In hafıza gereksinimlerini azaltmak için sipariş, `Mesh` Class tek bir örnek `Node` lass lass çeşitli örneklerine bağlı olabilir. Envision, tüm 3D küplerinin ayırt edilemez göründüğü bir sisteme ihtiyacınız var, ancak çok sayıda çok sayıda ihtiyacınız vardı. You sistem başladığında bir Mesh nesnesi yaparak bellek ayırabilir. At bu nokta, her zaman başka bir şekle ihtiyacınız olduğunda, başka bir Node nesnesi yaparsınız, sonra o düğmeyi bir `Mesh` olarak işaret edersiniz. This instancing olarak adlandırılır. 076. 481 076. 481 APIs instancing yapmak için izin verir.
### **Instancing örneği**
In RTS (Real-time strategy) gibi oyunlar, biz her zaman aynı 3D modeli ile birden fazla NPCs (Non-Player layer haracter) görebilirsiniz, belki farklı renklerde, işleme motoru genellikle aynı örgü geometri verilerini farklı NCCs arasında paylaşır, bu teknik Instancing olarak adlandırılır.

{{% alert color="primary" %}} 

The `Mesh` sınıf nesnesi kodda kullanılıyor. We can[Orada anlatılan Mesh sınıfı bir nesne oluşturun](https://docs.dynabic.com/display/3djava/Create+3D+Mesh+and+Scene).

{{% /alert %}} 

Örnek kodun stration emonstration:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-geometry-ShareMeshGeometryData.java" >}}


In bu örnek biz 3 küp düğümleri aynı örgü paylaşmak, her biri farklı renklerde farklı malzeme var.
