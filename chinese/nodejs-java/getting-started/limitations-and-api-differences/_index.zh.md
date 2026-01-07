---
title: 限制和 API 差异
type: docs
weight: 60
url: /zh/nodejs-java/limitations-and-api-differences/
keywords: nodejs, 3D, limitation, api, difference
description: Aspose.3D for Node.js via Java 限制和api差异
---
##  **公共 API 差异**
以下列表 (包含示例代码段) 显示了 Aspose.3D for Java 和 Aspose.3D for Node.js via Java api之间的一些差异。
###  **导入库 (包比较)**

**Aspose.3D for Java**

{{< highlight "java" >}}

 import com.aspose.threed.*;

{{< /highlight >}}


**Aspose.3D for Node.js via Java**

{{< highlight "java" >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

{{< /highlight >}}
###  **实例化新场景**

**Aspose.3D for Java**

{{< highlight "java" >}}

 Scene scene = new Scene();

{{< /highlight >}}


**Aspose.3D for Node.js via Java**

{{< highlight "java" >}}

var scene = new aspose.threed.Scene();

{{< /highlight >}}
###  **初始化对象**

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

##  **Aspose.3D for Node.js via Java API 与 Aspose 相比的其他限制。3D for Java API**
1. 不支持从数组，ArrayList，ResultSet等导入/导出数据。
1. 不支持打印。

