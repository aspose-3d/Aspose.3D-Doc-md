---
title: Primitive Form zu Mesh
type: docs
weight: 20
url: "/de/nodejs-java/primitive-shape-to-mesh/"
description: Aspose.3D für Node.js über die Java API unterstützt die Konvertierung jeder primitiven Form in ein Mesh. Primitive Formen umfassen die meisten grundlegenden und verwendeten Objekte wie Box, Kugel, Ebene, Zylinder und Torus.
---

## **Primitive Form in Mesh umwandeln**
Aspose.3D für Node.js über die Java API unterstützt die Umwandlung jeder primitiven Form in ein Mesh. Primitive Formen umfassen die meisten grundlegenden und verwendeten Objekte wie Box, Sphäre, Ebene, Zylinder und Torus.

{{% alert color="primary" %}}

Jede Klasse, die die Schnittstelle IMeshConvertible implementiert, kann in ein Mesh umgewandelt werden, während sie in ein beliebiges 3D-Dateiformat exportiert wird.

{{% /alert %}}
### **Sphäre-Primitive in Mesh umwandeln**
Eine Sphäre ist ein perfekt rundes geometrisches Objekt im dreidimensionalen Raum, das überall von Sportbällen bis hin zu Planeten im Weltraum zu finden ist. Verwenden wir das Sphären-Primitive, um ein Mesh zu erstellen.
Das Codebeispiel unten wandelt eine Sphäre in ein Mesh um.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// Objekt mit der Klasse Sphäre initialisieren
var convertible = new aspose.threed.Sphere();

// Sphäre in Mesh umwandeln
var mesh = convertible.toMesh();

{{< /highlight >}}

### **Box in Mesh umwandeln**
Eine Box beschreibt eine Vielzahl von Behältern und Aufbewahrungsmöglichkeiten für den dauerhaften Gebrauch als Lagerraum oder für die vorübergehende Verwendung, oft zum Transport von Inhalten. Verwenden wir das Box-Primitive, um ein Mesh zu erstellen. Das Codebeispiel unten wandelt eine Box in ein Mesh um.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// Objekt mit der Klasse Box initialisieren
var convertible = new aspose.threed.Box();

// Box in Mesh umwandeln
var mesh = convertible.toMesh();

{{< /highlight >}}

### **Eine Ebene in Mesh umwandeln**
Eine Ebene erstreckt sich unendlich ohne Dicke. Ein Beispiel für eine Ebene ist die Koordinatenebene. Verwenden wir das Ebenen-Primitive, um ein Mesh zu erstellen. Das Codebeispiel unten wandelt eine Ebene in ein Mesh um.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// Objekt mit der Klasse Plane initialisieren
var convertible = new aspose.threed.Plane();

// Ebene in Mesh umwandeln
var mesh = convertible.toMesh();

{{< /highlight >}}

### **Einen Zylinder in Mesh umwandeln**
Ein Zylinder ist eine der grundlegendsten gekrümmten geometrischen Formen, die Oberfläche, die durch die Punkte in fester Entfernung von einer gegebenen geraden Linie, der Achse des Zylinders, gebildet wird. Er kann an vielen Orten verwendet werden, zum Beispiel als Säule vor einem Haus oder als Antriebswelle eines Autos. Verwenden wir den Zylinder-Primitive, um ein Mesh zu erstellen. Das Codebeispiel unten wandelt einen Zylinder in ein Mesh um.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// Objekt mit der Klasse Cylinder initialisieren
var convertible = new aspose.threed.Cylinder();

// Zylinder in Mesh umwandeln
var mesh = convertible.toMesh();

{{< /highlight >}}

### **Einen Torus in Mesh umwandeln**
Ein Torus ist eine Oberfläche der Rotation, die durch die Rotation eines Kreises im dreidimensionalen Raum um eine Ebene zur Ebene des Kreises gebildet wird. Wenn die Rotationsachse den Kreis nicht berührt, hat die Oberfläche eine ringförmige Form und wird als Rotationstoroid bezeichnet. Verwenden wir den Torus-Primitive, um ein Mesh zu erstellen. Das Codebeispiel unten wandelt einen Torus in ein Mesh um.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// Objekt mit der Klasse Torus initialisieren
var convertible = new aspose.threed.Torus();

// Torus in Mesh umwandeln
var mesh = convertible.toMesh();

{{< /highlight >}}