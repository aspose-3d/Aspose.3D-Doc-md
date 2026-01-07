---
title: Geometrik Dönüşümü Açığa Çıkar
type: docs
weight: 50
url: "/tr/nodejs-java/expose-geometric-transformation/"
description: Aspose.3D for Node.js via Java, 3B boyutlu bir sahnenin geometrik dönüşümünü açığa çıkarma imkanı sunar. Küresel dönüşümü değerlendirmek için evaluateGlobalTransform yöntemini kullanabilirsiniz.
---

# **Geometrik Dönüşümü Açığa Çıkarın**
Aspose.3D for Node.js via Java, 3B sahnenin geometrik dönüşümünü açığa çıkarmayı sağlar. Küresel dönüşümü `evaluateGlobalTransform` metodu ile değerlendirebilirsiniz. Aşağıdaki kod parçacığı geometrik dönüşümü nasıl açığa çıkaracağınızı göstermektedir.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Sahne nesnesini başlatın
var scene = new aspose.threed.Scene();

// Silindiri başlatın
var cylinder =new aspose.threed.Cylinder();

// ChildNode Oluşturun
var Node=scene.getRootNode().createChildNode(cylinder);

// Geometrik Çeviriyi Alın
Node.getTransform().setGeometricTranslation(new aspose.threed.Vector3(10, 0, 0));

// İlk Console.WriteLine, geometrik dönüşümü içeren dönüşüm matrisini çıktı olarak verecektir
// ikinci ise vermeyecektir.
console.log(Node.evaluateGlobalTransform(true));
console.log(Node.evaluateGlobalTransform(false));

{{< /highlight >}}