---
title: Arbete med linjär Extrusion
type: docs
weight: 80
url: "/sv/nodejs-java/working-with-linear-extrusion/"
description: "Aspose.3D för Node.js via Java erbjuder klassen LinearExtrusion, som tar en 2D-form som indata och utökar formen i den 3:e dimensionen."
---

# **Utför Linjär Extrusion**
Aspose.3D för Node.js via Java erbjuder `LinearExtrusion`-klassen, som tar en 2D-form som indata och utökar formen i den 3:e dimensionen. Följande kodsnutt visar hur man utför linjär extrusion:

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Initialisera basformen som ska extruderad
// Initialisera basprofilen som ska extruderad
var profile=new aspose.threed.RectangleShape();
profile.setRoundingRadius(0.3);

// Utför linjär extrusion genom att skicka en 2D-form som indata och utöka formen i den 3:e dimensionen
var extrusion =new aspose.threed.LinearExtrusion(profile, 10);
extrusion.setSlices(100);
extrusion.setCenter(true);
extrusion.setTwist(360);
extrusion.setTwistOffset(new aspose.threed.Vector3(10, 0, 0));

// Skapa en scen
var scene = new aspose.threed.Scene();

// Skapa en underordnad nod genom att skicka extrusion
scene.getRootNode().createChildNode(extrusion);

// Spara 3D-scen
scene.save("LinearExtrusion.obj");

{{< /highlight >}}

# **Sektioner i Linjär Extrusion**
Aspose.3D för Node.js via Java erbjuder `setSlices()`-metoden för `LinearExtrusion`-klassen. `setSlices()`-metoden definierar antalet mellanliggande punkter längs extruderingens bana. Följande kodsnutt visar hur man använder `setSlices()`-metoden i linjär extrusion:

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Initialisera basprofilen som ska extruderad
var profile=new aspose.threed.RectangleShape();
profile.setRoundingRadius(0.3);

// Skapa en scen
var scene = new aspose.threed.Scene();

// Skapa vänster nod
var left=scene.getRootNode().createChildNode();
// Skapa höger nod
var right=scene.getRootNode().createChildNode();
left.getTransform().setTranslation(new aspose.threed.Vector3(5, 0, 0));

// Sektionsparametern definierar antalet mellanliggande punkter längs extruderingens bana
// Utför linjär extrusion på vänster nod med hjälp av egenskapen sektioner
var extrusion1 =new aspose.threed.LinearExtrusion(profile, 2);
extrusion1.setSlices(2);
left.createChildNode(extrusion1);

// Utför linjär extrusion på höger nod med hjälp av egenskapen sektioner
var extrusion2 =new aspose.threed.LinearExtrusion(profile, 2);
extrusion2.setSlices(10);
right.createChildNode(extrusion2);

// Spara 3D-scen
scene.save("SlicesInLinearExtrusion.obj");

{{< /highlight >}}

# **Centrera i Linjär Extrusion**
Aspose.3D för Node.js via Java erbjuder `setCenter()`-metoden för `LinearExtrusion`-klassen. Om `setCenter()`-metoden är inställd på true är extruderingens område från -Höjd/2 till Höjd/2, annars är extruderingen från 0 till Höjd. Följande kodsnutt visar hur man använder `setCenter()`-metoden i linjär extrusion:

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Initialisera basprofilen som ska extruderad
var profile=new aspose.threed.RectangleShape();
profile.setRoundingRadius(0.3);

// Skapa en scen
var scene = new aspose.threed.Scene();

// Skapa vänster nod
var left=scene.getRootNode().createChildNode();
// Skapa höger nod
var right=scene.getRootNode().createChildNode();
left.getTransform().setTranslation(new aspose.threed.Vector3(5, 0, 0));

// Ange markplan som referens
var box=new aspose.threed.Box(0.01, 3, 3);

// Om egenskapen Center är true är extruderingens område från -Höjd/2 till Höjd/2, annars är extruderingen från 0 till Höjd
// Utför linjär extrusion på vänster nod med hjälp av egenskaperna center och sektioner
var extrusion1 =new aspose.threed.LinearExtrusion(profile, 2);
extrusion1.setSlices(3);
extrusion1.setCenter(false);
left.createChildNode(extrusion1);
left.createChildNode(box);

// Utför linjär extrusion på höger nod med hjälp av egenskaperna center och sektioner
var extrusion2 =new aspose.threed.LinearExtrusion(profile, 2);
extrusion2.setSlices(3);
extrusion2.setCenter(true);
right.createChildNode(extrusion2);
right.createChildNode(box);

// Spara 3D-scen
scene.save("CenterInLinearExtrusion.obj");

{{< /highlight >}}

# **Vridning i Linjär Extrusion**
Aspose.3D för Node.js via Java erbjuder `setTwist()`-metoden för `LinearExtrusion`-klassen. `setTwist()`-metoden hanterar graden av rotation under extruderingen av formen. Följande kodsnutt visar hur man använder `setTwist()`-metoden i linjär extrusion:

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Initialisera basprofilen som ska extruderad
var profile=new aspose.threed.RectangleShape();
profile.setRoundingRadius(0.3);

// Skapa en scen
var scene = new aspose.threed.Scene();

// Skapa vänster nod
var left=scene.getRootNode().createChildNode();
// Skapa höger nod
var right=scene.getRootNode().createChildNode();
left.getTransform().setTranslation(new aspose.threed.Vector3(5, 0, 0));

// Vridningsegenskapen definierar graden av rotation under extruderingen av formen.
// Utför linjär extrusion på vänster nod med hjälp av egenskaperna sektioner och vridning
var extrusion1 =new aspose.threed.LinearExtrusion(profile, 10);
extrusion1.setSlices(100);
extrusion1.setTwist(360);
left.createChildNode(extrusion1);

// Utför linjär extrusion på höger nod med hjälp av egenskaperna vridning, sektioner och vridningsförskjutning
var extrusion2 =new aspose.threed.LinearExtrusion(profile, 10);
extrusion2.setSlices(100);
extrusion2.setTwist(360);
extrusion2.setTwistOffset(new aspose.threed.Vector3(3, 0, 0));
right.createChildNode(extrusion2);

// Spara 3D-scen
scene.save("TwistOffsetInLinearExtrusion.obj");

{{< /highlight >}}

# **Vridningsförskjutning i Linjär Extrusion**
Aspose.3D för Node.js via Java erbjuder `setTwistOffset()`-metoden för `LinearExtrusion`-klassen. `setTwistOffset()`-metoden definierar vridningsförskjutningen. Följande kodsnutt visar hur man använder `setTwistOffset()`-metoden i linjär extrusion:

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Initialisera basprofilen som ska extruderad
var profile=new aspose.threed.RectangleShape();
profile.setRoundingRadius(0.3);

// Skapa en scen
var scene = new aspose.threed.Scene();

// Skapa vänster nod
var left=scene.getRootNode().createChildNode();
// Skapa höger nod
var right=scene.getRootNode().createChildNode();
left.getTransform().setTranslation(new aspose.threed.Vector3(5, 0, 0));

// Vridningsförskjutningsegenskapen definierar vridningsförskjutningen.
// Utför linjär extrusion på vänster nod med hjälp av egenskaperna sektioner, vridning och vridningsförskjutning
var extrusion1 =new aspose.threed.LinearExtrusion(profile, 10);
extrusion1.setSlices(100);
extrusion1.setTwist(360);
left.createChildNode(extrusion1);

// Utför linjär extrusion på höger nod med hjälp av egenskaperna sektioner, vridning, vridningsförskjutning och vridningsförskjutning
var extrusion2 =new aspose.threed.LinearExtrusion(profile, 10);
extrusion2.setSlices(100);
extrusion2.setTwist(360);
extrusion2.setTwistOffset(new aspose.threed.Vector3(3, 0, 0));
right.createChildNode(extrusion2);

// Spara 3D-scen
scene.save("TwistOffsetInLinearExtrusion.obj");

{{< /highlight >}}

# **Riktning i Linjär Extrusion**
Aspose.3D för Node.js via Java erbjuder `setDirection()`-metoden för `LinearExtrusion`-klassen. `setDirection()`-metoden definierar riktningen för extruderingen. Följande kodsnutt visar hur man använder `setDirection()`-metoden i linjär extrusion:

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Initialisera basprofilen som ska extruderad
var profile=new aspose.threed.RectangleShape();
profile.setRoundingRadius(0.3);

// Skapa en scen
var scene = new aspose.threed.Scene();

// Skapa vänster nod
var left=scene.getRootNode().createChildNode();
// Skapa höger nod
var right=scene.getRootNode().createChildNode();
left.getTransform().setTranslation(new aspose.threed.Vector3(5, 0, 0));

// Riktningsegenskapen definierar riktningen för extruderingen.
// Utför linjär extrusion på vänster nod med hjälp av egenskaperna sektioner, vridning och vridningsförskjutning
var extrusion1 =new aspose.threed.LinearExtrusion(profile, 10);
extrusion1.setSlices(100);
extrusion1.setTwist(360);
left.createChildNode(extrusion1);

// Utför linjär extrusion på höger nod med hjälp av egenskaperna sektioner, vridning, vridningsförskjutning och riktning
var extrusion2 =new aspose.threed.LinearExtrusion(profile, 10);
extrusion2.setSlices(100);
extrusion2.setTwist(360);
extrusion2.setDirection(new aspose.threed.Vector3(0.3, 0.2, 1));
right.createChildNode(extrusion2);

// Spara 3D-scen
scene.save("DirectionInLinearExtrusion.obj");

{{< /highlight >}}