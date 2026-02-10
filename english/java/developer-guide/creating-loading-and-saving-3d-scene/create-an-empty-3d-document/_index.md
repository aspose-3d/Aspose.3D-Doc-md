---
title: Create an Empty 3D document
type: docs
weight: 20
url: /java/create-an-empty-3d-document/
description: Aspose.3D for Java API has support of creating 3D scene from scratch, and then save in supported 3D format.
---

## **Create an Empty 3D Scene and save in Supported 3D format**
Aspose.3D for Java API has support of creating 3D scene from scratch, and then save in supported 3D format.
### **Creating an Empty 3D Scene**
Please follow these steps to create a 3D Scene with Aspose.3D for Java API:

1. Create an instance of the **Scene** class that represents 3D scene.
1. Generate 3D document by calling the **save** method of the **Scene** class instance.
#### **Creating an Empty 3D Scene: Programming Samples**
{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
MyDir = MyDir + "document.fbx";
// Create an object of the Scene class
Scene scene = new Scene();
// Save 3D scene document
scene.save(MyDir, FileFormat.FBX7500ASCII);
{{< /highlight >}}




