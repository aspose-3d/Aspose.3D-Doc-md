---
title: Your First Aspose.3D Application
type: docs
weight: 30
url: /java/your-first-aspose-3d-application/
description: Create, edit and save your first 3d file in any supported formats using Aspose.3D for Java to experience its simplicity and power in Java.
keywords: Java , Aspose.3D for Java , The first application using Aspose.3D for Java, The first program via Aspose.3D for Java.
---

{{% alert color="primary" %}}

This tutorial explains how to create your first application using Aspose.3D's simple API. This simple application creates a 3d file in a specified 3D scene.

{{% /alert %}}

## **How to Create the Application**

The steps below creates the application using the Aspose.3D API:

1. Create an instance of the [Scene](https://reference.aspose.com/3d/java/com.aspose.threed/scene/) class.
1. If you have a license, then [apply it](/3d/java/licensing/).
   If you are using the evaluation version, skip the license related code lines.
1. Create a new 3D file, or open an existing 3D file.
1. Access the scene contents in the 3D file.
1. Generate the modified 3D file.

The implementation of the above steps is demonstrated in the examples below.

### **How to Create a New Scene Document**

The following example creates a new 3D scene file from scratch. First, create a 3D scene and then save the file in FBX format.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-CreateEmpty3DDocument.java" >}}

### **How to Open an Existing File**

The following example opens an existing 3D template file named "document.fbx" and then saves the 3D scene or document to a stream in various supported 3D formats.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-Save3DScene.java" >}}
