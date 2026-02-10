---
title: Working with VRML Format
type: docs
weight: 120
url: /net/working-with-vrml-format/
description: Aspose.3D for .NET allows working with VRML version 1.0. VRML file format has been added to the FileFormat class. Aspose.3D can auto detect the format, so the FileFormat is usually ignored in Open method. The following code snippet shows how open VRML file format.
---

{{% alert color="primary" %}} 

This feature is supported by version 19.4 or greater.

{{% /alert %}} 
# **Open VRML File Format**
Aspose.3D for .NET allows working with VRML version 1.0. `VRML` file format has been added to the `FileFormat` class. Aspose.3D can auto detect the format, so the `FileFormat` is usually ignored in `Open` method. The following code snippet shows how open VRML file format.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Create a Scene
Scene scene = new Scene();
// Open Virtual Reality Modeling Language (VRML) file format
scene.Open("test.wrl");
// Work with VRML file format...


{{< /highlight >}}
