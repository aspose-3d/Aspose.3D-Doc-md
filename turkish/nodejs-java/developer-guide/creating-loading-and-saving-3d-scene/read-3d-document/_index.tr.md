---
title: 3D belgeyi oku
type: docs
weight: 30
url: "/tr/nodejs-java/read-3d-document/"
description: Aspose.3D for Node.js Java API aracılığıyla çeşitli 3D belge türlerini okuma desteği bulunmaktadır.
---

## **3B Desteklenen Formatların Listesi (İçe Aktarma)**
Aspose.3D for Node.js Java API aracılığıyla çeşitli 3B belge türlerini okuma desteği bulunmaktadır. `Scene` sınıfının mevcut yapıcıları bunu yapmaya yardımcı olur ve geçerli bir dosya yolu dizesi kabul eder. Desteklenen okunabilir dosya formatları şunlardır:

1. FBX 7.5 (ASCII, Binary)
1. FBX 7.4 (ASCII, Binary)
1. FBX 7.3 (ASCII, Binary)
1. FBX 7.2 (ASCII, Binary)
1. STL (ASCII, Binary)
1. WavefrontOBJ
1. Discreet3DS
1. Universal3D
1. Collada
1. glTF
1. DXF
1. PLY (ASCII, Binary)
1. X (ASCII, Binary)
1. Draco
1. 3MF
1. RVM (Text, Binary)
1. ASE

Scene sınıfının yapıcıları 3B belge formatını dahili olarak algılar.
## **3B belgeyi İçe Aktarma**
Aspose.3D for Java API, değişiklik, ekleme ve işleme amaçları için çeşitli 3B belge türlerini içe aktarma desteği sunar.
### **3B Sahneyi Okuma: Programlama Örnekleri**

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// Bir Scene sınıfı nesnesi başlat
var scene = new aspose.threed.Scene();

// Mevcut bir 3B belgeyi yükle
scene.open( "document.obj");

{{< /highlight >}}