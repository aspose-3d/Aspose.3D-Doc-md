---
title: "Travailler avec l'extrusion linéaire"
type: docs
weight: 80
url: "/fr/nodejs-java/working-with-linear-extrusion/"
description: "Aspose.3D pour Node.js via Java offre la classe LinearExtrusion, qui prend une forme 2D en entrée et l'étend dans la 3ème dimension."
---

# **Effectuer une Extrusion Linéaire**
Aspose.3D pour Node.js via Java offre la classe `LinearExtrusion` qui prend une forme 2D comme entrée et étend la forme dans la 3ème dimension. Le code suivant montre comment effectuer une extrusion linéaire :

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// Initialiser la forme de base à extruder
// Initialiser le profil de base à extruder
var profile=new aspose.threed.RectangleShape();
profile.setRoundingRadius(0.3);

// Effectuer une extrusion linéaire en passant une forme 2D comme entrée et en étendant la forme dans la 3ème dimension
var extrusion =new aspose.threed.LinearExtrusion(profile, 10);
extrusion.setSlices(100);
extrusion.setCenter(true);
extrusion.setTwist(360);
extrusion.setTwistOffset(new aspose.threed.Vector3(10, 0, 0));

// Créer une scène
var scene = new aspose.threed.Scene();

// Créer un nœud enfant en passant l'extrusion
scene.getRootNode().createChildNode(extrusion);

// Sauvegarder la scène 3D
scene.save("LinearExtrusion.obj");

{{< /highlight >}}

# **Tranches dans une Extrusion Linéaire**
Aspose.3D pour Node.js via Java offre la méthode `setSlices` de la classe `LinearExtrusion`. La méthode setSlices définit le nombre de points intermédiaires le long du chemin de l'extrusion. Le code suivant montre comment utiliser la méthode setSlices dans une extrusion linéaire :

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// Initialiser le profil de base à extruder
var profile=new aspose.threed.RectangleShape();
profile.setRoundingRadius(0.3);

// Créer une scène
var scene = new aspose.threed.Scene();

// Créer un nœud gauche
var left=scene.getRootNode().createChildNode();
// Créer un nœud droit
var right=scene.getRootNode().createChildNode();
left.getTransform().setTranslation(new aspose.threed.Vector3(5, 0, 0));

// Le paramètre Slices définit le nombre de points intermédiaires le long du chemin de l'extrusion
// Effectuer une extrusion linéaire sur le nœud gauche en utilisant la propriété slices
var extrusion1 =new aspose.threed.LinearExtrusion(profile, 2);
extrusion1.setSlices(2);
left.createChildNode(extrusion1);

// Effectuer une extrusion linéaire sur le nœud droit en utilisant la propriété slices
var extrusion2 =new aspose.threed.LinearExtrusion(profile, 2);
extrusion2.setSlices(10);
right.createChildNode(extrusion2);

// Sauvegarder la scène 3D
scene.save("SlicesInLinearExtrusion.obj");

{{< /highlight >}}

# **Centre dans une Extrusion Linéaire**
Aspose.3D pour Node.js via Java offre la méthode `setCenter` de la classe `LinearExtrusion`. Si la méthode setCenter est définie sur true, la plage d'extrusion est de -Height/2 à Height/2, sinon, l'extrusion est de 0 à Height. Le code suivant montre comment utiliser la méthode setCenter dans une extrusion linéaire :

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// Initialiser le profil de base à extruder
var profile=new aspose.threed.RectangleShape();
profile.setRoundingRadius(0.3);

// Créer une scène
var scene = new aspose.threed.Scene();

// Créer un nœud gauche
var left=scene.getRootNode().createChildNode();
// Créer un nœud droit
var right=scene.getRootNode().createChildNode();
left.getTransform().setTranslation(new aspose.threed.Vector3(5, 0, 0));

// Définir un plan de base pour référence
var box=new aspose.threed.Box(0.01, 3, 3);

// Si la propriété Center est true, la plage d'extrusion est de -Height/2 à Height/2, sinon l'extrusion est de 0 à Height
// Effectuer une extrusion linéaire sur le nœud gauche en utilisant les propriétés center et slices
var extrusion1 =new aspose.threed.LinearExtrusion(profile, 2);
extrusion1.setSlices(3);
extrusion1.setCenter(false);
left.createChildNode(extrusion1);
left.createChildNode(box);

// Effectuer une extrusion linéaire sur le nœud droit en utilisant les propriétés center et slices
var extrusion2 =new aspose.threed.LinearExtrusion(profile, 2);
extrusion2.setSlices(3);
extrusion2.setCenter(true);
right.createChildNode(extrusion2);
right.createChildNode(box);

// Sauvegarder la scène 3D
scene.save("CenterInLinearExtrusion.obj");

{{< /highlight >}}

# **Torsion dans une Extrusion Linéaire**
Aspose.3D pour Node.js via Java offre la méthode `setTwist` de la classe `LinearExtrusion`. La méthode setTwist gère le degré de rotation pendant l'extrusion de la forme. Le code suivant montre comment utiliser la méthode setTwist dans une extrusion linéaire :

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// Initialiser le profil de base à extruder
var profile=new aspose.threed.RectangleShape();
profile.setRoundingRadius(0.3);

// Créer une scène
var scene = new aspose.threed.Scene();

// Créer un nœud gauche
var left=scene.getRootNode().createChildNode();
// Créer un nœud droit
var right=scene.getRootNode().createChildNode();
left.getTransform().setTranslation(new aspose.threed.Vector3(5, 0, 0));

// La propriété Direction définit la direction de l'extrusion.
// Effectuer une extrusion linéaire sur le nœud gauche en utilisant la propriété twist et slices
var extrusion1 =new aspose.threed.LinearExtrusion(profile, 10);
extrusion1.setSlices(100);
extrusion1.setTwist(360);
left.createChildNode(extrusion1);

// Effectuer une extrusion linéaire sur le nœud droit en utilisant la propriété twist, slices, et direction
var extrusion2 =new aspose.threed.LinearExtrusion(profile, 10);
extrusion2.setSlices(100);
extrusion2.setTwist(360);
extrusion2.setDirection(new aspose.threed.Vector3(0.3, 0.2, 1));
right.createChildNode(extrusion2);

// Sauvegarder la scène 3D
scene.save("DirectionInLinearExtrusion.obj");


{{< /highlight >}}

# **Décalage dans une Extrusion Linéaire**
Aspose.3D pour Node.js via Java offre la méthode `setTwistOffset` de la classe `LinearExtrusion`. La méthode setTwistOffset définit le décalage du degré de rotation pendant l'extrusion de la forme. Le code suivant montre comment utiliser la méthode setTwistOffset dans une extrusion linéaire :

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// Initialiser le profil de base à extruder
var profile=new aspose.threed.RectangleShape();
profile.setRoundingRadius(0.3);

// Créer une scène
var scene = new aspose.threed.Scene();

// Créer un nœud gauche
var left=scene.getRootNode().createChildNode();
// Créer un nœud droit
var right=scene.getRootNode().createChildNode();
left.getTransform().setTranslation(new aspose.threed.Vector3(5, 0, 0));

// La propriété Direction définit la direction de l'extrusion.
// Effectuer une extrusion linéaire sur le nœud gauche en utilisant la propriété twist et slices
var extrusion1 =new aspose.threed.LinearExtrusion(profile, 10);
extrusion1.setSlices(100);
extrusion1.setTwist(360);
left.createChildNode(extrusion1);

// Effectuer une extrusion linéaire sur le nœud droit en utilisant la propriété twist, slices, et direction
var extrusion2 =new aspose.threed.LinearExtrusion(profile, 10);
extrusion2.setSlices(100);
extrusion2.setTwist(360);
extrusion2.setTwistOffset(new aspose.threed.Vector3(3, 0, 0));
right.createChildNode(extrusion2);

// Sauvegarder la scène 3D
scene.save("TwistOffsetInLinearExtrusion.obj");

{{< /highlight >}}

# **Direction dans une Extrusion Linéaire**
Aspose.3D pour Node.js via Java offre la méthode `setDirection` de la classe `LinearExtrusion`. La méthode setDirection définit la direction de l'extrusion. Le code suivant montre comment utiliser la méthode setDirection dans une extrusion linéaire :

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// Initialiser le profil de base à extruder
var profile=new aspose.threed.RectangleShape();
profile.setRoundingRadius(0.3);

// Créer une scène
var scene = new aspose.threed.Scene();

// Créer un nœud gauche
var left=scene.getRootNode().createChildNode();
// Créer un nœud droit
var right=scene.getRootNode().createChildNode();
left.getTransform().setTranslation(new aspose.threed.Vector3(5, 0, 0));

// La propriété Direction définit la direction de l'extrusion.
// Effectuer une extrusion linéaire sur le nœud gauche en utilisant la propriété twist et slices
var extrusion1 =new aspose.threed.LinearExtrusion(profile, 10);
extrusion1.setSlices(100);
extrusion1.setTwist(360);
left.createChildNode(extrusion1);

// Effectuer une extrusion linéaire sur le nœud droit en utilisant la propriété twist, slices, et direction
var extrusion2 =new aspose.threed.LinearExtrusion(profile, 10);
extrusion2.setSlices(100);
extrusion2.setTwist(360);
extrusion2.setDirection(new aspose.threed.Vector3(0.3, 0.2, 1));
right.createChildNode(extrusion2);

// Sauvegarder la scène 3D
scene.save("DirectionInLinearExtrusion.obj");

{{< /highlight >}}