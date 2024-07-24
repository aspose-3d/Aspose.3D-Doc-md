---
title: Working with Linear Extrusion
type: docs
weight: 80
url: /nodejs-java/working-with-linear-extrusion/
description: Aspose.3D for Node.js via Java offers LinearExtrusion class, which takes a 2D shape as an input and extends the shape in the 3rd dimension.
---

# **Performing Linear Extrusion**
Aspose.3D for Node.js via Java offers `LinearExtrusion` class, which takes a 2D shape as an input and extends the shape in the 3rd dimension. Following code snippet shows how to perform linear extrusion:

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// Initialize the base shape to be extruded
// Initialize the base profile to be extruded
var profile=new aspose.threed.RectangleShape();
profile.setRoundingRadius(0.3);

// Perform Linear extrusion by passing a 2D shape as input and extend the shape in the 3rd dimension
var extrusion =new aspose.threed.LinearExtrusion(profile, 10);
extrusion.setSlices(100);
extrusion.setCenter(true);
extrusion.setTwist(360);
extrusion.setTwistOffset(new aspose.threed.Vector3(10, 0, 0));

// Create a scene
var scene = new aspose.threed.Scene();

// Create a child node by passing extrusion
scene.getRootNode().createChildNode(extrusion);

// Save 3D scene
scene.save("LinearExtrusion.obj");

{{< /highlight >}}

# **Slices in Linear Extrusion**
Aspose.3D for Node.js via Java offers `setSlices()` method of `LinearExtrusion` class. setSlices() method defines the number of intermediate points along the path of the extrusion. Following code snippet shows how to use setSlices() method in linear extrusion:

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// Initialize the base profile to be extruded
var profile=new aspose.threed.RectangleShape();
profile.setRoundingRadius(0.3);

// Create a scene
var scene = new aspose.threed.Scene();

// Create left node
var left=scene.getRootNode().createChildNode();
// Create right node
var right=scene.getRootNode().createChildNode();
left.getTransform().setTranslation(new aspose.threed.Vector3(5, 0, 0));

// Slices parameter defines the number of intermediate points along the path of the extrusion
// Perform linear extrusion on left node using slices property
var extrusion1 =new aspose.threed.LinearExtrusion(profile, 2);
extrusion1.setSlices(2);
left.createChildNode(extrusion1);

// Perform linear extrusion on right node using slices property
var extrusion2 =new aspose.threed.LinearExtrusion(profile, 2);
extrusion2.setSlices(10);
right.createChildNode(extrusion2);

// Save 3D scene
scene.save("SlicesInLinearExtrusion.obj");

{{< /highlight >}}

# **Center in Linear Extrusion**
Aspose.3D for Node.js via Java offers `setCenter()` method of `LinearExtrusion` class. If the setCenter() method is set to true, the extrusion range is from -Height/2 to Height/2, otherwise, the extrusion is from 0 to Height. Following code snippet shows how to use setCenter() method in linear extrusion:

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// Initialize the base profile to be extruded
var profile=new aspose.threed.RectangleShape();
profile.setRoundingRadius(0.3);

// Create a scene
var scene = new aspose.threed.Scene();

// Create left node
var left=scene.getRootNode().createChildNode();
// Create right node
var right=scene.getRootNode().createChildNode();
left.getTransform().setTranslation(new aspose.threed.Vector3(5, 0, 0));

// Set ground plane for reference
var box=new aspose.threed.Box(0.01, 3, 3);

// If Center property is true, the extrusion range is from -Height/2 to Height/2, otherwise the extrusion is from 0 to Height
// Perform linear extrusion on left node using center and slices property
var extrusion1 =new aspose.threed.LinearExtrusion(profile, 2);
extrusion1.setSlices(3);
extrusion1.setCenter(false);
left.createChildNode(extrusion1);
left.createChildNode(box);

// Perform linear extrusion on right node using center and slices property
var extrusion2 =new aspose.threed.LinearExtrusion(profile, 2);
extrusion2.setSlices(3);
extrusion2.setCenter(true);
right.createChildNode(extrusion2);
right.createChildNode(box);

// Save 3D scene
scene.save("CenterInLinearExtrusion.obj");

{{< /highlight >}}

# **Twist in Linear Extrusion**
Aspose.3D for Node.js via Java offers `setTwist()` method of `LinearExtrusion` class. The setTwist() method handles the degree of the rotation while extruding the shape. Following code snippet shows how to use setTwist() method in linear extrusion:

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// Initialize the base profile to be extruded
var profile=new aspose.threed.RectangleShape();
profile.setRoundingRadius(0.3);

// Create a scene
var scene = new aspose.threed.Scene();

// Create left node
var left=scene.getRootNode().createChildNode();
// Create right node
var right=scene.getRootNode().createChildNode();
left.getTransform().setTranslation(new aspose.threed.Vector3(5, 0, 0));

// Twist property defines the degree of the rotation while extruding the profile
// Perform linear extrusion on left node using twist and slices property
var extrusion1 =new aspose.threed.LinearExtrusion(profile, 10);
extrusion1.setSlices(100);
extrusion1.setTwist(0);
left.createChildNode(extrusion1);

// Perform linear extrusion on right node using twist and slices property
var extrusion2 =new aspose.threed.LinearExtrusion(profile, 10);
extrusion2.setSlices(100);
extrusion2.setTwist(90);
right.createChildNode(extrusion2);

// Save 3D scene
scene.save("TwistInLinearExtrusion.obj");

{{< /highlight >}}

# **TwistOffset in Linear Extrusion**
Aspose.3D for Node.js via Java offers `setTwistOffset()` method of `LinearExtrusion` class. The setTwistOffset() method translates offset while rotating the extrusion. Following code snippet shows how to use setTwistOffset() method in linear extrusion:

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// Initialize the base profile to be extruded
var profile=new aspose.threed.RectangleShape();
profile.setRoundingRadius(0.3);

// Create a scene
var scene = new aspose.threed.Scene();

// Create left node
var left=scene.getRootNode().createChildNode();
// Create right node
var right=scene.getRootNode().createChildNode();
left.getTransform().setTranslation(new aspose.threed.Vector3(5, 0, 0));

// TwistOffset property is the translate offset while rotating the extrusion.
// Perform linear extrusion on left node using twist and slices property
var extrusion1 =new aspose.threed.LinearExtrusion(profile, 10);
extrusion1.setSlices(100);
extrusion1.setTwist(360);
left.createChildNode(extrusion1);

// Perform linear extrusion on right node using twist, twist offset and slices property
var extrusion2 =new aspose.threed.LinearExtrusion(profile, 10);
extrusion2.setSlices(100);
extrusion2.setTwist(360);
extrusion2.setTwistOffset(new aspose.threed.Vector3(3, 0, 0));
right.createChildNode(extrusion2);

// Save 3D scene
scene.save("TwistOffsetInLinearExtrusion.obj");

{{< /highlight >}}

# **Direction in Linear Extrusion**
Aspose.3D for Node.js via Java offers `setDirection()` method of `LinearExtrusion` class. The setDirection() method defines the direction of the extrusion. Following code snippet shows how to use setDirection() method in linear extrusion:

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// Initialize the base profile to be extruded
var profile=new aspose.threed.RectangleShape();
profile.setRoundingRadius(0.3);

// Create a scene
var scene = new aspose.threed.Scene();

// Create left node
var left=scene.getRootNode().createChildNode();
// Create right node
var right=scene.getRootNode().createChildNode();
left.getTransform().setTranslation(new aspose.threed.Vector3(5, 0, 0));

// Direction property defines the direction of the extrusion.
// Perform linear extrusion on left node using twist and slices property
var extrusion1 =new aspose.threed.LinearExtrusion(profile, 10);
extrusion1.setSlices(100);
extrusion1.setTwist(360);
left.createChildNode(extrusion1);

// Perform linear extrusion on right node using twist, slices, and direction property
var extrusion2 =new aspose.threed.LinearExtrusion(profile, 10);
extrusion2.setSlices(100);
extrusion2.setTwist(360);
extrusion2.setDirection(new aspose.threed.Vector3(0.3, 0.2, 1));
right.createChildNode(extrusion2);

// Save 3D scene
scene.save("DirectionInLinearExtrusion.obj");


{{< /highlight >}}
