---
title: Limitations and API Differences
type: docs
weight: 60
url: /nodejs-java/limitations-and-api-differences/
keywords: "nodejs, 3D, limitation, api, differences"
description: "Aspose.3D for Node.js via Java limitations and api differences."
---

## **Public API Differences**
The following list (with sample code segments) shows some differences between Aspose.3D for Java and Aspose.3D for Node.js via Java APIs.
### **Importing library (Package Comparisons)**

**Aspose.3D for Java**

{{< highlight java >}}

 import com.aspose.threed.*;

{{< /highlight >}}


**Aspose.3D for Node.js via Java**

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

{{< /highlight >}}
### **Instantiating a new Scene**

**Aspose.3D for Java**

{{< highlight java >}}

 Scene scene = new Scene();

{{< /highlight >}}


**Aspose.3D for Node.js via Java**

{{< highlight java >}}

var scene = new aspose.threed.Scene();

{{< /highlight >}}
### **Initialize Object**

**Aspose.3D for Java**

{{< highlight java >}}

Plane plane = new Plane();

plane.setUp(new Vector3(1, 1, 3));

{{< /highlight >}}

**Aspose.3D for Node.js via Java**

{{< highlight java >}}

var plane=new aspose.threed.Plane();

plane.setUp(new aspose.threed.Vector3(1, 1, 3));

{{< /highlight >}}

## **Other Limitations of Aspose.3D for Node.js via Java API compared to Aspose.3D for Java API**
1. Importing/exporting data from an Array, ArrayList, ResultSet etc. is not supported.
1. Printing is not supported.

