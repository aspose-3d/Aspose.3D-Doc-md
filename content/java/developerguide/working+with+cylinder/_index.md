---
title : "Working with Cylinder" 
description : "" 
weight : 8051 
toc : false
type: docs
url: /java/developerguide/working+with+cylinder/
---

# Aspose.3D for Java : Working with Cylinder


{{< panel title="Contents Summary" style="primary" >}}
*   1 [Customize Offset Top](#customize-offset-top)
*   2 [Customize ShearBottom](#customize-shearbottom)
*   3 [Create FanCylinder](#create-fancylinder)
{{< /panel >}}
 

 

This feature is supported by version 19.6 or greater.

# Customize Offset Top

Aspose.3D for Java allows customizing Offset Top of a cylinder. In order to use this functionality, you can use **setOffsetTop()** method of **Cylinder** class. The following code snippet shows how to customize Offset Top:

![image](https://docs2.aspose.com/3d/java/attachments/92176441/92340227.png)

The left one has OffsetTop set to (5, 3, 0), it's easy to see the top cap has moved and the whole torso also gets affected.

# Customize ShearBottom

Aspose.3D for Java allows customizing shear bottom of a cylinder. In order to use this functionality, you can use **setShearBottom()** property of **Cylinder** class. The following code snippet shows how to customize Shear Bottom:

![image](https://docs2.aspose.com/3d/java/attachments/92176441/92340226.png)

The left cylinder has ShearBottom to (0, 0.83) while the right one is an ordinal cylinder.

# Create FanCylinder

Aspose.3D for Java allows creating a fan cylinder. In order to use this functionality, you can **setGenerateFanCylinder()** property of **Cylinder** class to **True.** The following code snippet shows how to use this functionality:

![image](https://docs2.aspose.com/3d/java/attachments/92176441/92340225.png)

The left cylinder has GenerateFanCylinder = false and the right one has GenerateFanCylinder = true.

