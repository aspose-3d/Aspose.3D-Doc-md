---
title: Arbetar med VRML Format
type: docs
weight: 90
url: /sv/nodejs-java/working-with-vrml-format/
description: Aspose.3D for Node.js via Java tillåter att arbeta med VRML version 1.0. VRML filformat har lagts till i klassen FileFormat. Aspose.3D kan automatiskt detektera VRML-formatet, så filformatet ignoreras vanligtvis i Öppna metoden.
---
#  **Open VRML File Format**
Aspose.3D for Node.js via Java tillåter att arbeta med VRML version 1.0. `VRML` filformat har lagts till i `FileFormat` klassen. Aspose.3D kan automatiskt detektera `VRML`-formatet, så `FileFormat` ignoreras vanligtvis i Öppningsmetoden. Följande kodsnutt visar hur öppet VRML filformat.

{{< highlight "java" >}}

// initialize a scene
var scene = new aspose.threed.Scene();

// open Virtual Reality Modeling Language (VRML) file format
scene.open( "test.wrl");

{{< /highlight >}}
