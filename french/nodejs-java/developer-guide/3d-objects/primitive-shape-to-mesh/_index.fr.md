---
title: Forme primitive vers maillage
type: docs
weight: 20
url: "/fr/nodejs-java/primitive-shape-to-mesh/"
description: "Aspose.3D pour Node.js via l'API Java prend en charge la conversion de n'importe quelle forme primitive en maillage. Les formes primitives incluent les objets les plus basiques et couramment utilisés comme le cube, la sphère, le plan, le cylindre et le tore."
---

## **Convertir une Forme Primitive en Maille**
Aspose.3D pour Node.js via l'API Java prend en charge la conversion de n'importe quelle forme primitive en maille. Les formes primitives incluent les objets les plus basiques et les plus utilisés tels que le cube, la sphère, le plan, le cylindre et le tore.

{{% alert color="primary" %}}

Toute classe qui implémente l'interface IMeshConvertible peut être convertie en maille lors de l'exportation vers n'importe quel format de fichier 3D.

{{% /alert %}}
### **Convertir une Sphère Primitive en Maille**
Une sphère est un objet géométrique parfaitement rond dans l'espace tridimensionnel que l'on retrouve partout, des ballons de sport aux planètes dans l'espace. Utilisons la primitive Sphère pour créer une maille.
L'exemple de code ci-dessous convertit une Sphère en maille.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Initialiser l'objet par la classe Sphère
var convertible = new aspose.threed.Sphere();

// Convertir une Sphère en Maille
var mesh = convertible.toMesh();

{{< /highlight >}}

### **Convertir un Cube en Maille**
Un Cube décrit une variété de conteneurs et de réceptacles pour un usage permanent comme stockage, ou pour un usage temporaire, souvent pour le transport de contenu. Utilisons la primitive Cube pour créer une maille. L'exemple de code ci-dessous convertit un Cube en maille.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Initialiser l'objet par la classe Cube
var convertible = new aspose.threed.Box();

// Convertir un Cube en Maille
var mesh = convertible.toMesh();

{{< /highlight >}}

### **Convertir un Plan en Maille**
Un plan s'étend à l'infini sans épaisseur. Un exemple de plan est un plan de coordonnées. Utilisons la primitive Plan pour créer une maille. L'exemple de code ci-dessous convertit un Plan en maille.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Initialiser l'objet par la classe Plan
var convertible = new aspose.threed.Plane();

// Convertir un Plan en Maille
var mesh = convertible.toMesh();

{{< /highlight >}}

### **Convertir un Cylindre en Maille**
Un cylindre est l'une des formes géométriques courbes les plus basiques, la surface formée par les points à une distance fixe d'une ligne droite donnée, l'axe du cylindre. Il peut être utilisé dans de nombreux endroits, par exemple comme pilier devant une maison ou comme arbre de transmission de voiture. Utilisons la primitive Cylindre pour créer une maille. L'exemple de code ci-dessous convertit un Cylindre en maille.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Initialiser l'objet par la classe Cylindre
var convertible = new aspose.threed.Cylinder();

// Convertir un Cylindre en Maille
var mesh = convertible.toMesh();

{{< /highlight >}}

### **Convertir un Tore en Maille**
Un tore est une surface de révolution générée en faisant tourner un cercle dans l'espace tridimensionnel autour d'un axe coplanaire avec le cercle. Si l'axe de révolution ne touche pas le cercle, la surface a une forme d'anneau et est appelée tore de révolution. Utilisons la primitive Tore pour créer une maille. L'exemple de code ci-dessous convertit un Tore en maille.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Initialiser l'objet par la classe Tore
var convertible = new aspose.threed.Torus();

// Convertir un Tore en Maille
var mesh = convertible.toMesh();

{{< /highlight >}}