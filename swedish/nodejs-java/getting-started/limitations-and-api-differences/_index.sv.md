---
title: Begränsningar och API Skillnader
type: docs
weight: 60
url: /sv/nodejs-java/limitations-and-api-differences/
keywords: nodejs, 3D, limitation, api, difference
description: Aspose.3D for Node.js via Java begränsningar och api skillnader
---
##  **Offentlig API Skillnader**
Följande lista (med exempelkodsegment) visar några skillnader mellan Aspose.3D for Java och Aspose.3D for Node.js via Java API.
###  **Importera bibliotek (paketjämförelser)**

**Aspose.3D for Java**

{{< highlight "java" >}}

 import com.aspose.threed.*;

{{< /highlight >}}


**Aspose.3D for Node.js via Java**

{{< highlight "java" >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

{{< /highlight >}}
###  **Att styrka en ny scenp**

**Aspose.3D for Java**

{{< highlight "java" >}}

 Scene scene = new Scene();

{{< /highlight >}}


**Aspose.3D for Node.js via Java**

{{< highlight "java" >}}

var scene = new aspose.threed.Scene();

{{< /highlight >}}
###  **Initiera objekt**

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

##  **Andra begränsningar för Aspose.3D for Node.js via Java API jämfört med Aspose.3D for Java API**
1. Import/exportering av data från en Array, ArrayList, ResultSet etc. stöds inte.
1. Utskrift stöds inte.

