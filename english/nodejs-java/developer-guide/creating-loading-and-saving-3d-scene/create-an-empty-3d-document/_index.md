---
title: Create an Empty 3D document
type: docs
weight: 20
url: /nodejs-java/create-an-empty-3d-document/
description: Aspose.3D for Node.js via Java API has support of creating 3D scene from scratch, and then save in supported 3D format.
---

## **Create an Empty 3D Scene and save in Supported 3D format**
Aspose.3D for Node.js via Java API has support of creating 3D scene from scratch, and then save in supported 3D format.
### **Creating an Empty 3D Scene**
Please follow these steps to create a 3D Scene with Aspose.3D for Node.js via Java API:

1. Create an instance of the **Scene** class that represents 3D scene.
1. Generate 3D document by calling the **save** method of the **Scene** class instance.
#### **Creating an Empty 3D Scene: Programming Samples**
{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

var file="document.fbx";

// Create an object of the Scene class
var scene = new aspose.threed.Scene();

// Save 3D scene document
scene.save(file);

{{< /highlight >}}




