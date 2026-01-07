---
title: Limites et différences API
type: docs
weight: 60
url: /fr/nodejs-java/limitations-and-api-differences/
keywords: nodejs, 3D, limitation, api, difference
description: Aspose.3D for Node.js via Java limitations et différences d'api
---
##  **Public API Différences**
La liste suivante (avec des exemples de segments de code) montre quelques différences entre les API Aspose.3D for Java et Aspose.3D for Node.js via Java.
###  **Importation de bibliothèque (comparaisons de packages)**

**Aspose.3D for Java**

{{< highlight "java" >}}

 import com.aspose.threed.*;

{{< /highlight >}}


**Aspose.3D for Node.js via Java**

{{< highlight "java" >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

{{< /highlight >}}
###  **Instanciation d'une nouvelle scène**

**Aspose.3D for Java**

{{< highlight "java" >}}

 Scene scene = new Scene();

{{< /highlight >}}


**Aspose.3D for Node.js via Java**

{{< highlight "java" >}}

var scene = new aspose.threed.Scene();

{{< /highlight >}}
###  **Initialiser l'objet**

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

##  **Autres limites de Aspose.3D for Node.js via Java API par rapport à Aspose.3D for Java API**
1. L'importation/exportation de données à partir d'un tableau, ArrayList, ResultSet, etc. n'est pas prise en charge.
1. L'impression n'est pas prise en charge.

