---
title: Einschränkungen und API Unterschiede
type: docs
weight: 60
url: /de/nodejs-java/limitations-and-api-differences/
keywords: nodejs, 3D, limitation, api, difference
description: Aspose.3D for Node.js via Java Einschränkungen und Api-Unterschiede
---
##  **Öffentliche API Unterschiede**
Die folgende Liste (mit Beispielcode-Segmenten) zeigt einige Unterschiede zwischen Aspose.3D for Java und Aspose.3D for Node.js via Java APIs.
###  **Import bibliothek (Paket vergleiche)**

**Aspose.3D for Java**

{{< highlight "java" >}}

 import com.aspose.threed.*;

{{< /highlight >}}


**Aspose.3D for Node.js via Java**

{{< highlight "java" >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

{{< /highlight >}}
###  **Eine neue Szene installieren**

**Aspose.3D for Java**

{{< highlight "java" >}}

 Scene scene = new Scene();

{{< /highlight >}}


**Aspose.3D for Node.js via Java**

{{< highlight "java" >}}

var scene = new aspose.threed.Scene();

{{< /highlight >}}
###  **Objekt initial isieren**

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

##  **Andere Einschränkungen von Aspose.3D for Node.js via Java API im Vergleich zu Aspose.3D for Java API**
1. Das Importieren/Exportieren von Daten aus einem Array, Array List, ResultSet usw. wird nicht unterstützt.
1. Das Drucken wird nicht unterstützt.

