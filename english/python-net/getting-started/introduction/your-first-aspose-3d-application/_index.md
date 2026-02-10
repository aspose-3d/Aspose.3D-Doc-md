---
title: Your First Aspose.3D Application
type: docs
weight: 30
url: /python-net/your-first-aspose-3d-application/
---

{{% alert color="primary" %}}

This tutorial explains how to create your first application using Aspose.3D's simple API. This simple application creates a 3d file in a specified 3D scene.

{{% /alert %}}

## **How to Create the Application**

The steps below creates the application using the Aspose.3D API:

1. Create an instance of the [Scene](https://reference.aspose.com/3d/python-net/aspose.threed/scene/) class.
1. If you have a license, then [apply it](/3d/python-net/licensing/).
   If you are using the evaluation version, skip the license related code lines.
1. Create a new 3D file, or open an existing 3D file.
1. Access the scene contents in the 3D file.
1. Generate the modified 3D file.

The implementation of the above steps is demonstrated in the examples below.

### **How to Create a New Scene Document** 

The following example creates a new 3D scene file from scratch. First, create a 3D scene and then save the file in FBX format.

{{< highlight "python" >}}
import aspose.threed as a3d
# For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
# The path to the documents directory.
# Create an object of the Scene class
scene = a3d.Scene()
# Save 3D scene document
scene.Save("document.fbx", a3d.FileFormat.FBX7500ASCII)
{{< /highlight >}}

### **How to Open an Existing File**

The following example opens an existing 3D template file named "document.fbx".

{{< highlight "python" >}}
import aspose.threed as a3d
# For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
# The path to the documents directory.

# Initialize a Scene class object
scene = Scene()
# Load an existing 3D document
scene.open("document.fbx")
{{< /highlight >}}
