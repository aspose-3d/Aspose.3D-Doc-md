---
title: Specify 3D File Load Options
type: docs
weight: 10
url: /nodejs-java/specify-3d-file-load-options/
description: There are several Scene.open method overloads or Scene class constructor overloads that accept LoadOptions instance.
---

## **3D File Load Options**
There are several Scene.open method overloads or Scene class constructor overloads that accept LoadOptions instance. This should be an instance of a class derived from the LoadOptions class. Each load format has a corresponding class that holds load options for that load format, for example there is ColladaSaveOptions for the FileFormat.COLLADA save format.
### **Use of the Discreet 3DS Load Options**
The code below shows how to set load options before loading a Discreet 3DS file.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

var loadOpts = new aspose.threed.Discreet3dsLoadOptions();

// Sets wheather to use the transformation defined in the first frame of animation track.
loadOpts.setApplyAnimationTransform(true);

// Flip the coordinate system
loadOpts.setFlipCoordinateSystem(true);

// Prefer to use gamma-corrected color if a 3ds file provides both original color and gamma-corrected color.
loadOpts.setGammaCorrectedColor(true);

{{< /highlight >}}

### **Use of the Obj Load Options**
The code below shows how to set load options before loading an 3D Obj file.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

var loadObjOpts  = new aspose.threed.ObjLoadOptions();

// Import materials from external material library file
loadObjOpts.setEnableMaterials(true);

// Flip the coordinate system.
loadObjOpts.setFlipCoordinateSystem(true);

{{< /highlight >}}

### **Use of the STL Load Options**
The code below shows how to set load options before loading an STL file.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Initialize an object
var loadSTLOpts   = new aspose.threed.StlLoadOptions();

// Flip the coordinate system.
loadSTLOpts.setFlipCoordinateSystem(true);

{{< /highlight >}}

### **Use of the U3D Load Options**
The code below shows how to set load options before loading a U3D file.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Initialize an object
var loadU3DOpts = new aspose.threed.U3dLoadOptions();

// Flip the coordinate system.
loadU3DOpts.setFlipCoordinateSystem(true);

{{< /highlight >}}

### **Use of the glTF Load Options**
The code below shows how to set load options before loading a glTF file.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Set load options
var loadOpt = new aspose.threed.GltfLoadOptions();

// The default value is true, usually we don't need to change it. Aspose.3D will automatically flip the V/T texture coordinate during load and save.
loadOpt.setFlipTexCoordV(true);

{{< /highlight >}}

### **Use of the Ply Load Options**
The code below shows how to set load options before loading a PLY model.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// initialize Scene class object
var scene = new aspose.threed.Scene();

// initialize an object
var loadPLYOpts  = new aspose.threed.PlyLoadOptions();

// Flip the coordinate system.
loadPLYOpts.setFlipCoordinateSystem(true);

// load 3D Ply model
scene.open("vase-v2.ply", loadPLYOpts);

{{< /highlight >}}

### **Use of the DirectX X Load Options**
The code below shows how to set load options before loading a DirectX X file.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// initialize Scene class object
var scene = new aspose.threed.Scene();

// initialize an object
var loadXOpts = new aspose.threed.XLoadOptions(aspose.threed.FileContentType.ASCII);

// flip the coordinate system.
loadXOpts.setFlipCoordinateSystem(true);

// load 3D X file
scene.open("warrior.x", loadXOpts);

{{< /highlight >}}

### **Use FBX Load Options**

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

//This will output all properties defined in GlobalSettings in FBX file.
var opt = new aspose.threed.FbxLoadOptions();

opt.setKeepBuiltinGlobalSettings(true);

{{< /highlight >}}
