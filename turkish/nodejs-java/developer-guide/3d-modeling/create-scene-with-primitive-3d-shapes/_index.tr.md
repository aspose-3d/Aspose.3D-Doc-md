---
title: Basit 3B Şekillerle Sahne Oluştur
type: docs
weight: 20
url: "/tr/nodejs-java/create-scene-with-primitive-3d-shapes/"
description: "Aspose.3D for Node.js Java API aracılığıyla ilkel 3B şekiller desteği bulunmaktadır. Tüm parametreli ilkel şekiller, herhangi bir desteklenen çıktı dosya biçiminde kaydederken otomatik olarak mesh'e dönüştürülecektir."
---

{{% alert color="primary" %}} 

Aspose.3D for Node.js via Java API, temel 3B şekiller desteği içerir. Tüm parametreli şekiller, herhangi bir desteklenen çıktı dosya formatında kaydederken otomatik olarak mesh'e dönüştürülür.

{{% /alert %}} 
## **Temel 3B Şekillerden Sahne Oluşturma**
Modelleme, saf yaratım sürecidir ve Aspose.3D API, temel 3B şekillerle bir sahne oluşturmayı destekler.
### **Programlama Örneği**
Bu kod örneği, temel 3B şekillerle bir sahne oluşturur ve OBJ dosyasında kaydeder.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// 3B sahneyi başlat
var scene = new aspose.threed.Scene();

// Bir Box modeli oluştur
scene.getRootNode().createChildNode("box", new aspose.threed.Box());

// Bir Cylinder modeli oluştur
scene.getRootNode().createChildNode("cylinder", new aspose.threed.Cylinder());

// Çizimi OBJ formatında kaydet
scene.save("test.obj");


{{< /highlight >}}