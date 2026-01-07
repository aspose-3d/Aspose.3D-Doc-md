---
title: 3B Nesnelere Malzeme Ekle
type: docs
weight: 60
url: "/tr/nodejs-java/add-material-to-3d-entities/"
description: "PBR, oyun motoru görselleri için önemli bir rol oynar; ışık ile yüzey arasındaki etkileşimlerin parlaklığın zayıflaması ve yansıyan ışığın saçılması yoluyla verimli ve gerçekçi bir şekilde oluşturulmasını sağlar. Geliştiriciler, Aspose.3D API'sini kullanarak bir sahnedeki 3B nesnelere PBR malzemesi uygulayabilirler. Bu kod örneği, bir Box nesnesi oluşturmayı ve ardından PBR malzemesi uygulamayı göstermektedir."
---

{{% alert color="primary" %}}

PBR, oyun motoru görselleri için önemli bir rol oynar; parlaklığın zayıflaması ve yansıyan ışığın saçılması yoluyla ışık ve yüzey arasındaki etkileşimlerin verimli ve gerçekçi bir şekilde oluşturulmasını sağlar. Geliştiriciler, PBR malzemesini bir sahnedeki 3D nesnelere uygulamak için Aspose.3D API'sini kullanabilirler. Bu kod örneği, bir Box nesnesi oluşturmayı ve ardından PBR malzemesini uygulamayı göstermektedir.

{{% /alert %}}


## **Bir Kutuya Fiziksel Tabanlı Render (PBR) Malzemesi Uygulama**

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// bir sahneyi başlat
var scene = new aspose.threed.Scene();

// PBR malzeme nesnesini başlat
var mat = new aspose.threed.PbrMaterial();

// neredeyse metalik bir malzeme
mat.setMetallicFactor(0.9);

// malzeme yüzeyi çok pürüzlü
mat.setRoughnessFactor(0.9);

// malzeme uygulanacak bir kutu oluştur
var boxNode = scene.getRootNode().createChildNode("box", new aspose.threed.Box());
boxNode.setMaterial(mat);

// 3B sahneyi USDZ formatında kaydet
scene.save("PBR_Material_Box_Out.usdz");

{{< /highlight >}}