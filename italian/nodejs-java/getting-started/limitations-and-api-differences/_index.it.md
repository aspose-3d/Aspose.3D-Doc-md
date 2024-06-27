---
title: Limitazioni e API Differenze
type: docs
weight: 60
url: /it/nodejs-java/limitations-and-api-differences/
keywords: nodejs, 3D, limitation, api, difference
description: Aspose.3D for Node.js via Java limitazioni e differenze api
---
##  **Differenze pubbliche di API**
L'elenco seguente (con segmenti di codice di esempio) mostra alcune differenze tra Aspose.3D for Java e Aspose.3D for Node.js via Java API.
###  **Importazione della libreria (Confronti dei pacchetti)**

**Aspose.3D for Java**

{{< highlight "java" >}}

 import com.aspose.threed.*;

{{< /highlight >}}


**Aspose.3D for Node.js via Java**

{{< highlight "java" >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

{{< /highlight >}}
###  **Istantanea di una nuova scena**

**Aspose.3D for Java**

{{< highlight "java" >}}

 Scene scene = new Scene();

{{< /highlight >}}


**Aspose.3D for Node.js via Java**

{{< highlight "java" >}}

var scene = new aspose.threed.Scene();

{{< /highlight >}}
###  **Inizializzare l'oggetto**

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

##  **Altre limitazioni di Aspose.3D for Node.js via Java API rispetto a Aspose.3D for Java API**
1. L'importazione/esportazione di dati da un array, ArrayList, ResultSet ecc. non è supportata.
1. La stampa non è supportata.

