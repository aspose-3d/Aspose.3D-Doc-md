---
title: Working with VRML Format
type: docs
weight: 90
url: /nodejs-java/working-with-vrml-format/
description: Aspose.3D for Node.js via Java allows working with VRML version 1.0. VRML file format has been added to the FileFormat class. Aspose.3D can auto detect VRML format, so the FileFormat is usually ignored in Open method.
---

# **Open VRML File Format**
Aspose.3D for Node.js via Java allows working with VRML version 1.0. `VRML` file format has been added to the `FileFormat` class. Aspose.3D can auto detect `VRML` format, so the `FileFormat` is usually ignored in Open method. The following code snippet shows how open VRML file format.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// initialize a scene
var scene = new aspose.threed.Scene();

// open Virtual Reality Modeling Language (VRML) file format
scene.open( "test.wrl");

{{< /highlight >}}
