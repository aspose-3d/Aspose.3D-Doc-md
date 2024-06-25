---
title: Limitaciones y diferencias de API
type: docs
weight: 60
url: /es/nodejs-java/limitations-and-api-differences/
keywords: nodejs, 3D, limitation, api, difference
description: Aspose.3D for Node.js via Java limitaciones y diferencias de api
---
##  **Diferencias públicas API**
La siguiente lista (con segmentos de código de muestra) muestra algunas diferencias entre las API Aspose.3D for Java y Aspose.3D for Node.js via Java.
###  **Importar biblioteca (Comparaciones de paquetes)**

**Aspose.3D for Java**

{{< highlight "java" >}}

 import com.aspose.threed.*;

{{< /highlight >}}


**Aspose.3D for Node.js via Java**

{{< highlight "java" >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

{{< /highlight >}}
###  **Instanciar una nueva escena**

**Aspose.3D for Java**

{{< highlight "java" >}}

 Scene scene = new Scene();

{{< /highlight >}}


**Aspose.3D for Node.js via Java**

{{< highlight "java" >}}

var scene = new aspose.threed.Scene();

{{< /highlight >}}
###  **Initialize (objeto)**

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

##  **Otras limitaciones de Aspose.3D for Node.js via Java API en comparación con Aspose.3D for Java API**
1. No se admite la importación/exportación de datos desde un Array, ArrayList, ResultSet, etc.
1. La impresión no es compatible.

