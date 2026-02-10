---
title: Your First Aspose.3D Application
type: docs
weight: 30
url: /net/your-first-aspose-3d-application/
description: Create, edit and save your first 3d file in any supported formats using Aspose.3D for .NET to experience its simplicity and power in C#.
keywords: C# , Aspose.3D for .NET , The first application using Aspose.3D for .NET, The first program via Aspose.3D for .NET.
---

{{% alert color="primary" %}}

This tutorial explains how to create your first application using Aspose.3D's simple API. This simple application creates a 3d file in a specified 3D scene.

{{% /alert %}}

## **How to Create the Application**

The steps below creates the application using the Aspose.3D API:

1. Create an instance of the [Scene](https://reference.aspose.com/3d/net/aspose.threed/scene/) class.
1. If you have a license, then [apply it](/3d/net/licensing/).
   If you are using the evaluation version, skip the license related code lines.
1. Create a new 3D file, or open an existing 3D file.
1. Access the scene contents in the 3D file.
1. Generate the modified 3D file.

The implementation of the above steps is demonstrated in the examples below.

### **How to Create a New Scene Document**

The following example creates a new 3D scene file from scratch. First, create a 3D scene and then save the file in FBX format.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET

// Create an object of the Scene class
Scene scene = new Scene();
// Save 3D scene document
scene.Save("document.fbx");

{{< /highlight >}}

### **How to Open an Existing File**

The following example opens an existing 3D template file named "document.fbx" and then saves the 3D scene or document to a stream in various supported 3D formats.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
                        
// Load a 3D document into Aspose.3D
Scene scene = new Scene();

// Open an existing 3D scene
scene.Open("document.fbx");

// Save Scene to a stream
MemoryStream dstStream = new MemoryStream();
scene.Save(dstStream, FileFormat.FBX7500ASCII);
            
// Save Scene to a local path
scene.Save("output_out.fbx");

{{< /highlight >}}
