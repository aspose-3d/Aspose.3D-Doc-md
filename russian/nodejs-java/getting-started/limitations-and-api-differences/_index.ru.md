---
title: Ограничения и API отличий
type: docs
weight: 60
url: /ru/nodejs-java/limitations-and-api-differences/
keywords: nodejs, 3D, limitation, api, difference
description: Ограничения Aspose.3D for Node.js via Java и различия api
---
##  **Публичный API Различия**
Следующий список (с примерами сегментов кода) показывает некоторые различия между Aspose.3D for Java и Aspose.3D for Node.js via Java API.
###  **Импорт библиотеки (Сравнение пакетов)**

**Aspose.3D for Java**

{{< highlight "java" >}}

 import com.aspose.threed.*;

{{< /highlight >}}


**Aspose.3D for Node.js via Java**

{{< highlight "java" >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

{{< /highlight >}}
###  **Становление новой сцены**

**Aspose.3D for Java**

{{< highlight "java" >}}

 Scene scene = new Scene();

{{< /highlight >}}


**Aspose.3D for Node.js via Java**

{{< highlight "java" >}}

var scene = new aspose.threed.Scene();

{{< /highlight >}}
###  **Инициализировать объект**

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

##  **Другие ограничения Aspose.3D for Node.js via Java API по сравнению с Aspose.3D for Java API**
1. Импорт/экспорт данных из массива, ArrayList, ResultSet и т. д. не поддерживается.
1. Печать не поддерживается.

