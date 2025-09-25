---
title: "Node'a Dönüşüm Ekleniyor"
type: docs
weight: 10
url: "/tr/nodejs-java/adding-transformation-to-the-node/"
description: "Aspose.3D for Node.js Java API aracılığıyla 3B uzayda nesneleri döndürme desteği bulunmaktadır. Nesnenin 3B uzaydaki rotasyonunu tanımlamak için üç yol vardır: Euler açıları, Quaternion ve Özel Matris, bunların hepsi Transform sınıfı tarafından desteklenmektedir."
---

{{% alert color="primary" %}} 

Aspose.3D for Node.js via Java API, 3D uzayda nesneleri döndürme desteğine sahiptir. Nesnenin 3D uzaydaki rotasyonunu tanımlamanın üç yolu vardır: Euler açıları, Quaternion ve Özel Matris, bunların hepsi `Transform` sınıfı tarafından desteklenir.

{{% /alert %}} 

TSR (Çeviri/Ölçekleme/Döndürme), 3D senaryolarda en yaygın olarak kullanılır, Aspose.3D'de bunları erişmek için bir `Transform` sınıfı sağladık. Afin dönüşümler şunları içerir:

- Çeviri
- Ölçekleme
- Döndürme
- Kaydırma eşleme
- Sıkıştırma eşleme

## **Euler Açıları ile Döndürme**

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// Sahne nesnesini başlat
var scene = new aspose.threed.Scene();

// Silindiri başlat
var cylinder =new aspose.threed.Cylinder(2, 2, 10, 20, 1, false);

// Çocuk Düğüm Oluştur
var Node=scene.getRootNode().createChildNode(cylinder);

// Euler açıları
Node.getTransform().setEulerAngles(new aspose.threed.Vector3(30, 40, 50));

// Çeviri ayarla
Node.getTransform().setTranslation(new aspose.threed.Vector3(0, 0, 20));

// Kaydet
scene.save("TransformationToNode.obj");

{{< /highlight >}}

## **Özel Dönüşüm Matrisi**
Ayrıca Matris'i doğrudan da kullanabiliriz:

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// Sahne nesnesini başlat
var scene = new aspose.threed.Scene();

// Silindiri başlat
var cylinder =new aspose.threed.Cylinder(2, 2, 10, 20, 1, false);

// Çocuk Düğüm Oluştur
var Node=scene.getRootNode().createChildNode(cylinder);

// Özel çeviri matrisini ayarla
Node.getTransform().setTransformMatrix(new aspose.threed.Matrix4(
    1, -0.3, 0, 0,
    0.4, 1, 0.3, 0,
    0, 0, 1, 0,
    0, 20, 0, 1
));

// Kaydet
scene.save("TransformationToNode.obj");

{{< /highlight >}}
