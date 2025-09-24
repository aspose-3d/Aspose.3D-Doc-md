---
title: Temel Şekli Ağa
type: docs
weight: 20
url: "/tr/nodejs-java/primitive-shape-to-mesh/"
description: Aspose.3D for Node.js Java API aracılığıyla, herhangi bir basit geometrik şekli ağa dönüştürme desteği bulunmaktadır. Basit geometrik şekiller, kutu, küre, düzlem, silindir ve torus gibi en temel ve yaygın olarak kullanılan nesneleri içerir.
---

## **Basit Şekilleri Ağa Dönüştürün**
Aspose.3D for Node.js, Java API aracılığıyla herhangi bir basit şekli ağa dönüştürme desteğine sahiptir. Basit şekiller, kutu, küre, düzlem, silindir ve torus gibi en temel ve yaygın olarak kullanılan nesneleri içerir.

{{% alert color="primary" %}}

IMeshConvertible arayüzünü uygulayan herhangi bir sınıf, herhangi bir 3D dosya biçimine aktarılırken ağa dönüştürülebilir.

{{% /alert %}}
### **Küre Basitini Ağa Dönüştürün**
Bir küre, üç boyutlu uzayda mükemmel derecede yuvarlak bir geometrik nesnedir ve spor toplarından gezegenlere kadar her yerde karşımıza çıkar. Küre basitini kullanarak bir ağ oluşturalım.
Aşağıdaki kod örneği bir Küreyi ağa dönüştürür.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// Nesneyi Küre sınıfı ile başlatın
var convertible = new aspose.threed.Sphere();

// Bir Küreyi Ağa Dönüştürün
var mesh = convertible.toMesh();

{{< /highlight >}}

### **Kutuyu Ağa Dönüştürün**
Bir Kutu, kalıcı olarak depolama için veya genellikle içerikleri taşımak için geçici olarak kullanılan çeşitli kapları ve muhafazaları tanımlar. Kutu basitini kullanarak bir ağ oluşturalım. Aşağıdaki kod örneği bir Kutuyu ağa dönüştürür.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// Nesneyi Kutu sınıfı ile başlatın
var convertible = new aspose.threed.Box();

// Bir Kutuyu Ağa Dönüştürün
var mesh = convertible.toMesh();

{{< /highlight >}}

### **Bir Düzlemi Ağa Dönüştürün**
Bir düzlem sonsuz olarak kalınlık olmadan uzanır. Bir düzlemin örneği bir koordinat düzlemidir. Düzlem basitini kullanarak bir ağ oluşturalım. Aşağıdaki kod örneği bir Düzlemi ağa dönüştürür.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// Nesneyi Düzlem sınıfı ile başlatın
var convertible = new aspose.threed.Plane();

// Bir Düzlemi Ağa Dönüştürün
var mesh = convertible.toMesh();

{{< /highlight >}}

### **Bir Silindiri Ağa Dönüştürün**
Bir silindir, verilen düz bir çizgi olan eksen etrafında dönerek oluşan en temel eğrisel geometrik şekillerden biridir. Bir silindir, örneğin bir evin önündeki bir sütun veya bir otomobil tahrik mili gibi birçok yerde kullanılabilir. Silindir basitini kullanarak bir ağ oluşturalım. Aşağıdaki kod örneği bir Silindiri ağa dönüştürür.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// Nesneyi Silindir sınıfı ile başlatın
var convertible = new aspose.threed.Cylinder();

// Bir Silindiri Ağa Dönüştürün
var mesh = convertible.toMesh();

{{< /highlight >}}

### **Bir Torusu Ağa Dönüştürün**
Bir torus, üç boyutlu uzayda bir dairenin bir eksen etrafında döndürülmesiyle oluşturulan bir dönüşüm yüzeyidir. Eksen dönme eksenine dokunmayan eksen için yüzey bir halka şeklindedir ve dönüşüm torusu olarak adlandırılır. Torus basitini kullanarak bir ağ oluşturalım. Aşağıdaki kod örneği bir Torusu ağa dönüştürür.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// Nesneyi Torus sınıfı ile başlatın
var convertible = new aspose.threed.Torus();

// Bir Torusu Ağa Dönüştürün
var mesh = convertible.toMesh();

{{< /highlight >}}