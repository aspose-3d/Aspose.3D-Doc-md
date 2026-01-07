---
title: Sınırlamalar ve API farklılıklar
type: docs
weight: 60
url: /tr/nodejs-java/limitations-and-api-differences/
keywords: nodejs, 3D, limitation, api, difference
description: Aspose.3D for Node.js via Java sınırlamalar ve api farklılıkları
---
##  **Kamu API farklılıklar**
Aşağıdaki liste (örnek kod segmentleri ile) Aspose arasında bazı farklar gösterir. 3D for Java ve Aspose.3D for Node.js via Java apis.
###  **Kütüphane ithalatı (paket karşılaştırmaları)**

**Aspose.3D for Java**

{{< highlight "java" >}}

 import com.aspose.threed.*;

{{< /highlight >}}


**Aspose.3D for Node.js via Java**

{{< highlight "java" >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

{{< /highlight >}}
###  **Yeni bir sahne kurmak**

**Aspose.3D for Java**

{{< highlight "java" >}}

 Scene scene = new Scene();

{{< /highlight >}}


**Aspose.3D for Node.js via Java**

{{< highlight "java" >}}

var scene = new aspose.threed.Scene();

{{< /highlight >}}
###  **Nesneyi başlat**

**Aspose.3D for Java**

{{< highlight "java" >}}

Plane plane = new Plane();

plane.setUp(new Vector3(1, 1, 3));

{{< /highlight >}}

**Aspose.3D for Node.js via Java**

{{< highlight "java" >}}

var plane=new aspose.threed.Plane();

plane.setUp(new aspose.threed.Vector3(1, 1, 3));

{{< /highlight >}}

##  **Other Limitations of Aspose.3D for Node.js via Java API compared to Aspose.3D for Java API**
1. Bir dizinin verilerini içe aktarma/dışa aktarma, arraylist, sonuç seti vb. desteklenmiyor.
1. Baskı desteklenmiyor.

