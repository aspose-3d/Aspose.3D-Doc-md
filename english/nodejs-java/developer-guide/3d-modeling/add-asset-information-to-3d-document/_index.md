---
title: Add Asset Information to 3D document
type: docs
weight: 10
url: /nodejs-java/add-asset-information-to-3d-document/
description: Metadata is structured information that describes, explains, locates or makes it easier to retrieve, use or manage an information resource. Aspose.3D for Node.js via Java API has support to define Metadata for the scene.
---

## **Add Asset Information to 3D document**
Metadata is structured information that describes, explains, locates or makes it easier to retrieve, use or manage an information resource. Aspose.3D for Node.js via Java API has support to define Metadata for the scene.
### **Define a Metadata for the scene**
3D shows produce massive quantities of metadata and picture information. Metadata is an asset and part of the show.

1. Initialize a 3D Scene using `Scene` class.
1. Set application/tool name.
1. Set application/tool vendor name.
1. Set measurement unit.
1. Set measurement unit scale factor.
1. Save 3D scene in the supported file format.

In this example, we assume the scene is created by a CAD tool called “Egypt” and it’s designed by “Manualdesk”:

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// Initialize a 3D scene
var scene = new aspose.threed.Scene();

// Initialize the Box object
var box=new aspose.threed.Box();

// Add the Box object to the scene
scene.getRootNode().createChildNode(box);

// Set application/tool name
scene.getAssetInfo().setApplicationName("Egypt");

// Set application/tool vendor name
scene.getAssetInfo().setApplicationVendor("Manualdesk");

// We use ancient egyption measurement unit Pole
scene.getAssetInfo().setUnitName("pole");

// One Pole equals to 60cm
scene.getAssetInfo().setUnitScaleFactor(0.6);

scene.save("InformationToScene.obj");

{{< /highlight >}}
