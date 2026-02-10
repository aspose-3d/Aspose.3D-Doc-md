---
title: Arbetar med VRML Format
type: docs
weight: 120
url: /sv/net/working-with-vrml-format/
description: Aspose.3D for .NET tillåter arbete med VRML version 1.0. VRML filformat har lagts till i klassen FileFormat. Aspose.3D kan automatiskt detektera formatet, så filformatet ignoreras vanligtvis i Öppna metoden. Följande kodsnutt visar hur öppet VRML filformat.
---
{{% alert color="primary" %}} 

Denna funktion stöds av version 19.4 eller större.

{{% /alert %}} 
#  **Open VRML File Format**
Aspose.3D for .NET tillåter arbete med VRML version 1.0. `VRML` filformat har lagts till i `FileFormat` klassen. Aspose.3D kan automatiskt detektera formatet, så `FileFormat` ignoreras vanligtvis i `Open`-metoden. Följande kodsnutt visar hur öppet VRML filformat.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Create a Scene
Scene scene = new Scene();
// Open Virtual Reality Modeling Language (VRML) file format
scene.Open("test.wrl");
// Work with VRML file format...


{{< /highlight >}}
