---
title: 3D Dosya Yükleme Seçeneklerini Belirtin
type: docs
weight: 10
url: "/tr/nodejs-java/specify-3d-file-load-options/"
description: Birkaç tane Scene.open metodu aşırı yüklemesi veya Scene sınıfı yapıcısı aşırı yüklemesi, LoadOptions örneği alır.
---

## **3D Dosya Yükleme Seçenekleri**
Aşağıdaki Scene.open yöntem yüklemesi veya Scene sınıfı yapıcısının aşırı yüklemeleri LoadOptions nesnesini kabul eder. Bu, LoadOptions sınıfından türetilen bir sınıfın bir örneği olmalıdır. Her yükleme biçiminin, o yükleme biçimi için yükleme seçeneklerini içeren ilgili bir sınıfı vardır; örneğin, FileFormat.COLLADA kaydetme biçimi için ColladaSaveOptions vardır.
### **Discreet 3DS Yükleme Seçeneklerinin Kullanımı**
Aşağıdaki kod, bir Discreet 3DS dosyası yüklemeden önce yükleme seçeneklerini ayarlamanın nasıl yapıldığını gösterir.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

var loadOpts = new aspose.threed.Discreet3dsLoadOptions();

// Animasyon parçasının ilk karesinde tanımlanan dönüşümü kullanıp kullanmayacağını ayarlar.
loadOpts.setApplyAnimationTransform(true);

// Koordinat sistemini ters çevir
loadOpts.setFlipCoordinateSystem(true);

// 3ds dosyası hem orijinal rengi hem de gama düzeltilmiş rengi sağlıyorsa, gama düzeltilmiş rengi tercih edin.
loadOpts.setGammaCorrectedColor(true);

{{< /highlight >}}

### **Obj Yükleme Seçeneklerinin Kullanımı**
Aşağıdaki kod, bir 3D Obj dosyası yüklemeden önce yükleme seçeneklerini ayarlamanın nasıl yapıldığını gösterir.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

var loadObjOpts  = new aspose.threed.ObjLoadOptions();

// Dış malzeme kitaplık dosyasından malzemeleri içe aktar
loadObjOpts.setEnableMaterials(true);

// Koordinat sistemini ters çevir.
loadObjOpts.setFlipCoordinateSystem(true);

{{< /highlight >}}

### **STL Yükleme Seçeneklerinin Kullanımı**
Aşağıdaki kod, bir STL dosyası yüklemeden önce yükleme seçeneklerini ayarlamanın nasıl yapıldığını gösterir.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Bir nesne başlat
var loadSTLOpts   = new aspose.threed.StlLoadOptions();

// Koordinat sistemini ters çevir.
loadSTLOpts.setFlipCoordinateSystem(true);

{{< /highlight >}}

### **U3D Yükleme Seçeneklerinin Kullanımı**
Aşağıdaki kod, bir U3D dosyası yüklemeden önce yükleme seçeneklerini ayarlamanın nasıl yapıldığını gösterir.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Bir nesne başlat
var loadU3DOpts = new aspose.threed.U3dLoadOptions();

// Koordinat sistemini ters çevir.
loadU3DOpts.setFlipCoordinateSystem(true);

{{< /highlight >}}

### **glTF Yükleme Seçeneklerinin Kullanımı**
Aşağıdaki kod, bir glTF dosyası yüklemeden önce yükleme seçeneklerini ayarlamanın nasıl yapıldığını gösterir.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Yükleme seçeneklerini ayarlayın
var loadOpt = new aspose.threed.GltfLoadOptions();

// Varsayılan değer doğrudur, genellikle bunu değiştirmemize gerek yoktur. Aspose.3D, yükleme ve kaydetme sırasında V/T doku koordinatını otomatik olarak ters çevirecektir.
loadOpt.setFlipTexCoordV(true);

{{< /highlight >}}

### **Ply Yükleme Seçeneklerinin Kullanımı**
Aşağıdaki kod, bir PLY modeli yüklemeden önce yükleme seçeneklerini ayarlamanın nasıl yapıldığını gösterir.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Scene sınıfı nesnesini başlat
var scene = new aspose.threed.Scene();

// Bir nesne başlat
var loadPLYOpts  = new aspose.threed.PlyLoadOptions();

// Koordinat sistemini ters çevir.
loadPLYOpts.setFlipCoordinateSystem(true);

// 3D Ply modeli yükle
scene.open("vase-v2.ply", loadPLYOpts);

{{< /highlight >}}

### **DirectX X Yükleme Seçeneklerinin Kullanımı**
Aşağıdaki kod, bir DirectX X dosyası yüklemeden önce yükleme seçeneklerini ayarlamanın nasıl yapıldığını gösterir.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Scene sınıfı nesnesini başlat
var scene = new aspose.threed.Scene();

// Bir nesne başlat
var loadXOpts = new aspose.threed.XLoadOptions(aspose.threed.FileContentType.ASCII);

// Koordinat sistemini ters çevir.
loadXOpts.setFlipCoordinateSystem(true);

// 3D X dosyasını yükle
scene.open("warrior.x", loadXOpts);

{{< /highlight >}}

### **FBX Yükleme Seçenekleri**

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Bu, FBX dosyasındaki GlobalSettings'te tanımlanan tüm özellikleri çıktılayacaktır.
var opt = new aspose.threed.FbxLoadOptions();

opt.setKeepBuiltinGlobalSettings(true);

{{< /highlight >}}