---
title: Working with Cylinder
type: docs
weight: 100
url: /java/working-with-cylinder/
---

{{% alert color="primary" %}} 

This feature is supported by version 19.6 or greater.

{{% /alert %}} 
# **Customize Offset Top**
Aspose.3D for Java allows customizing Offset Top of a cylinder. In order to use this functionality, you can use **setOffsetTop()** method of **Cylinder** class. The following code snippet shows how to customize Offset Top:



{{< gist "aspose-com-gists" "0672215ca08d7566bd64d657e2b228a7" "CustomizedOffsetTopCylinder.java" >}}

![todo:image_alt_text](working-with-cylinder_1.png)

The left one has OffsetTop set to (5, 3, 0), it's easy to see the top cap has moved and the whole torso also gets affected.
# **Customize ShearBottom**
Aspose.3D for Java allows customizing shear bottom of a cylinder. In order to use this functionality, you can use **setShearBottom()** property of **Cylinder** class. The following code snippet shows how to customize Shear Bottom:



{{< gist "aspose-com-gists" "0672215ca08d7566bd64d657e2b228a7" "CustomizedShearBottomCylinder.java" >}}

![todo:image_alt_text](working-with-cylinder_2.png)

The left cylinder has ShearBottom to (0, 0.83) while the right one is an ordinal cylinder.
# **Create Fan-Cylinder**
Aspose.3D for Java allows creating a fan cylinder. In order to use this functionality, you can **setGenerateFanCylinder()** property of **Cylinder** class to **True.** The following code snippet shows how to use this functionality:



{{< gist "aspose-com-gists" "0672215ca08d7566bd64d657e2b228a7" "CreateFanCylinder.java" >}}

![todo:image_alt_text](working-with-cylinder_3.png)

The left cylinder has GenerateFanCylinder = false and the right one has GenerateFanCylinder = true.
