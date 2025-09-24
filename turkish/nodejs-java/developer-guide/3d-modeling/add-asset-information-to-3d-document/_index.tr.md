---
title: 3B belgesine Varlık Bilgisi ekleyin
type: docs
weight: 10
url: "/tr/nodejs-java/add-asset-information-to-3d-document/"
description: Metaveri, bir bilgi kaynağını tanımlamak, açıklamak, konumlandırmak veya almayı, kullanmayı veya yönetmeyi kolaylaştırmak için kullanılan yapılandırılmış bilgidir. Aspose.3D for Node.js Java API aracılığıyla sahne için Metaveri tanımlama desteği bulunmaktadır.
---

## **3B Belgeye Varlık Bilgisi Ekleme**
Meta veri, bir bilgi kaynağını tanımlamak, açıklamak, konumlandırmak veya almayı, kullanmayı veya yönetmeyi kolaylaştırmak için yapılandırılmış bilgidir. Aspose.3D for Node.js Java API aracılığıyla sahne için Meta veri tanımlama desteği vardır.
### **Sahne için Meta veri Tanımlama**
3B gösterileri, büyük miktarlarda meta veri ve resim bilgisi üretir. Meta veri bir varlıktır ve gösterinin bir parçasıdır.

1. `Scene` sınıfını kullanarak bir 3B sahneyi başlatın.
1. Uygulama/araç adı ayarla.
1. Uygulama/araç satıcı adı ayarla.
1. Ölçü birimi ayarla.
1. Ölçü birimi ölçek faktörü ayarla.
1. 3B sahneyi desteklenen dosya biçiminde kaydedin.

Bu örnekte, sahnenin “Egypt” adlı bir CAD aracı tarafından oluşturulduğunu ve “Manualdesk” tarafından tasarlandığını varsayıyoruz:

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// 3B sahneyi başlatın
var scene = new aspose.threed.Scene();

// Box nesnesini başlatın
var box=new aspose.threed.Box();

// Box nesnesini sahneye ekleyin
scene.getRootNode().createChildNode(box);

// Uygulama/araç adı ayarla
scene.getAssetInfo().setApplicationName("Egypt");

// Uygulama/araç satıcı adı ayarla
scene.getAssetInfo().setApplicationVendor("Manualdesk");

// Antik Mısır ölçü birimi Pole kullanıyoruz
scene.getAssetInfo().setUnitName("pole");

// Bir Pole 60cm'ye eşittir
scene.getAssetInfo().setUnitScaleFactor(0.6);

scene.save("InformationToScene.obj");

{{< /highlight >}}