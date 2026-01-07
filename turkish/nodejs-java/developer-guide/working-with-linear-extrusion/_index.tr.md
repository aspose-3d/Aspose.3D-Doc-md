---
title: Doğrusal Ekstrüzyon ile Çalışma
type: docs
weight: 80
url: "/tr/nodejs-java/working-with-linear-extrusion/"
description: Aspose.3D for Node.js via Java, LineerEkstrüzyon sınıfını sunar ve bu sınıf 2B bir şekli girdi olarak alır ve şekli 3. boyutta uzatır.
---

# **Doğrusal Ekstrüzyon İşlemi**
Aspose.3D for Node.js via Java, `LinearExtrusion` sınıfını sunar ve bu sınıf, bir 2B şekli girdi olarak alır ve şekli 3. boyutta uzatır. Aşağıdaki kod parçacığı doğrusal ekstrüzyon işleminin nasıl yapılacağını gösterir:

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Temel profili ekstrüzyona başlamak için başlat
// Temel profili ekstrüzyona başlamak için başlat
var profile=new aspose.threed.RectangleShape();
profile.setRoundingRadius(0.3);

// Girdi olarak 2B bir şekil alarak ve şekli 3. boyutta uzatarak doğrusal ekstrüzyon gerçekleştirin
var extrusion =new aspose.threed.LinearExtrusion(profile, 10);
extrusion.setSlices(100);
extrusion.setCenter(true);
extrusion.setTwist(360);
extrusion.setTwistOffset(new aspose.threed.Vector3(10, 0, 0));

// Bir sahne oluşturun
var scene = new aspose.threed.Scene();

// Ekstrüzyonu geçirerek bir alt düğüm oluşturun
scene.getRootNode().createChildNode(extrusion);

// 3B sahneyi kaydedin
scene.save("LinearExtrusion.obj");

{{< /highlight >}}

# **Doğrusal Ekstrüzyonda Dilimler**
Aspose.3D for Node.js via Java, `LinearExtrusion` sınıfının `setSlices()` metodunu sunar. setSlices() metodu, ekstrüzyon yolu boyunca ara noktaların sayısını tanımlar. Aşağıdaki kod parçacığı, doğrusal ekstrüzyonda setSlices() metodunun nasıl kullanılacağını gösterir:

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Temel profili ekstrüzyona başlamak için başlat
var profile=new aspose.threed.RectangleShape();
profile.setRoundingRadius(0.3);

// Bir sahne oluşturun
var scene = new aspose.threed.Scene();

// Sol düğümü oluşturun
var left=scene.getRootNode().createChildNode();
// Sağ düğümü oluşturun
var right=scene.getRootNode().createChildNode();
left.getTransform().setTranslation(new aspose.threed.Vector3(5, 0, 0));

// Dilimler parametresi, ekstrüzyon yolu boyunca ara noktaların sayısını tanımlar
// Sol düğümde dilim özelliğini kullanarak doğrusal ekstrüzyon gerçekleştirin
var extrusion1 =new aspose.threed.LinearExtrusion(profile, 2);
extrusion1.setSlices(2);
left.createChildNode(extrusion1);

// Sağ düğümde dilim özelliğini kullanarak doğrusal ekstrüzyon gerçekleştirin
var extrusion2 =new aspose.threed.LinearExtrusion(profile, 2);
extrusion2.setSlices(10);
right.createChildNode(extrusion2);

// 3B sahneyi kaydedin
scene.save("SlicesInLinearExtrusion.obj");

{{< /highlight >}}

# **Doğrusal Ekstrüzyonda Merkez**
Aspose.3D for Node.js via Java, `LinearExtrusion` sınıfının `setCenter()` metodunu sunar. setCenter() metodu true olarak ayarlanırsa, ekstrüzyon aralığı -Yükseklik/2'den Yükseklik/2'ye kadar olur, aksi takdirde ekstrüzyon 0'dan Yükseklik'e kadar olur. Aşağıdaki kod parçacığı, doğrusal ekstrüzyonda setCenter() metodunun nasıl kullanılacağını gösterir:

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Temel profili ekstrüzyona başlamak için başlat
var profile=new aspose.threed.RectangleShape();
profile.setRoundingRadius(0.3);

// Bir sahne oluşturun
var scene = new aspose.threed.Scene();

// Sol düğümü oluşturun
var left=scene.getRootNode().createChildNode();
// Sağ düğümü oluşturun
var right=scene.getRootNode().createChildNode();
left.getTransform().setTranslation(new aspose.threed.Vector3(5, 0, 0));

// Referans için zemin düzlemini ayarlayın
var box=new aspose.threed.Box(0.01, 3, 3);

// Merkez özelliği true ise, ekstrüzyon aralığı -Yükseklik/2'den Yükseklik/2'ye kadar olur, aksi takdirde ekstrüzyon 0'dan Yükseklik'e kadar olur
// Sol düğümde merkez ve dilim özelliklerini kullanarak doğrusal ekstrüzyon gerçekleştirin
var extrusion1 =new aspose.threed.LinearExtrusion(profile, 2);
extrusion1.setSlices(3);
extrusion1.setCenter(false);
left.createChildNode(extrusion1);
left.createChildNode(box);

// Sağ düğümde merkez ve dilim özelliklerini kullanarak doğrusal ekstrüzyon gerçekleştirin
var extrusion2 =new aspose.threed.LinearExtrusion(profile, 2);
extrusion2.setSlices(3);
extrusion2.setCenter(true);
right.createChildNode(extrusion2);
right.createChildNode(box);

// 3B sahneyi kaydedin
scene.save("CenterInLinearExtrusion.obj");

{{< /highlight >}}

# **Doğrusal Ekstrüzyonda Büküm**
Aspose.3D for Node.js via Java, `LinearExtrusion` sınıfının `setTwist()` metodunu sunar. setTwist() metodu, ekstrüzyonun dönüş açısını tanımlar. Aşağıdaki kod parçacığı, doğrusal ekstrüzyonda setTwist() metodunun nasıl kullanılacağını gösterir:

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Temel profili ekstrüzyona başlamak için başlat
var profile=new aspose.threed.RectangleShape();
profile.setRoundingRadius(0.3);

// Bir sahne oluşturun
var scene = new aspose.threed.Scene();

// Sol düğümü oluşturun
var left=scene.getRootNode().createChildNode();
// Sağ düğümü oluşturun
var right=scene.getRootNode().createChildNode();
left.getTransform().setTranslation(new aspose.threed.Vector3(5, 0, 0));

// Büküm parametresi, ekstrüzyonun dönüş açısını tanımlar
// Sol düğümde büküm ve dilim özelliklerini kullanarak doğrusal ekstrüzyon gerçekleştirin
var extrusion1 =new aspose.threed.LinearExtrusion(profile, 10);
extrusion1.setSlices(100);
extrusion1.setTwist(360);
left.createChildNode(extrusion1);

// Sağ düğümde büküm, büküm ofseti ve dilim özelliklerini kullanarak doğrusal ekstrüzyon gerçekleştirin
var extrusion2 =new aspose.threed.LinearExtrusion(profile, 10);
extrusion2.setSlices(100);
extrusion2.setTwist(360);
extrusion2.setTwistOffset(new aspose.threed.Vector3(3, 0, 0));
right.createChildNode(extrusion2);

// 3B sahneyi kaydedin
scene.save("TwistOffsetInLinearExtrusion.obj");

{{< /highlight >}}

# **Doğrusal Ekstrüzyonda Yön**
Aspose.3D for Node.js via Java, `setDirection()` metodunu sunar. setDirection() metodu, ekstrüzyonun yönünü tanımlar. Aşağıdaki kod parçacığı, doğrusal ekstrüzyonda setDirection() metodunun nasıl kullanılacağını gösterir:

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Temel profili ekstrüzyona başlamak için başlat
var profile=new aspose.threed.RectangleShape();
profile.setRoundingRadius(0.3);

// Bir sahne oluşturun
var scene = new aspose.threed.Scene();

// Sol düğümü oluşturun
var left=scene.getRootNode().createChildNode();
// Sağ düğümü oluşturun
var right=scene.getRootNode().createChildNode();
left.getTransform().setTranslation(new aspose.threed.Vector3(5, 0, 0));

// Yön parametresi, ekstrüzyonun yönünü tanımlar
// Sol düğümde büküm ve dilim özelliklerini kullanarak doğrusal ekstrüzyon gerçekleştirin
var extrusion1 =new aspose.threed.LinearExtrusion(profile, 10);
extrusion1.setSlices(100);
extrusion1.setTwist(360);
left.createChildNode(extrusion1);

// Sağ düğümde büküm, dilim ve yön özelliklerini kullanarak doğrusal ekstrüzyon gerçekleştirin
var extrusion2 =new aspose.threed.LinearExtrusion(profile, 10);
extrusion2.setSlices(100);
extrusion2.setTwist(360);
extrusion2.setDirection(new aspose.threed.Vector3(0.3, 0.2, 1));
right.createChildNode(extrusion2);

// 3B sahneyi kaydedin
scene.save("DirectionInLinearExtrusion.obj");


{{< /highlight >}}