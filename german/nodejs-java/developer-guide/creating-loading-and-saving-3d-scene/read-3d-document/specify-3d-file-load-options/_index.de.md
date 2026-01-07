---
title: "3D-Datei-Ladeoptionen angeben"
type: docs
weight: 10
url: "/de/nodejs-java/specify-3d-file-load-options/"
description: "Es gibt mehrere überladene Scene.open-Methoden oder überladene Scene-Klassenkonstruktoren, die eine LoadOptions-Instanz akzeptieren."
---

## **3D-Datei-Ladeoptionen**
Es gibt mehrere Scene.open Methodenüberladungen oder Scene Klassenkonstruktionsüberladungen, die eine LoadOptions Instanz akzeptieren. Dies sollte eine Instanz einer Klasse sein, die von der LoadOptions Klasse abgeleitet ist. Jedes Dateiformat hat eine entsprechende Klasse, die Ladeoptionen für dieses Dateiformat enthält, beispielsweise ColladaSaveOptions für das FileFormat.COLLADA Speicherformat.
### **Verwendung der Discreet 3DS-Ladeoptionen**
Der folgende Code zeigt, wie Ladeoptionen vor dem Laden einer Discreet 3DS-Datei festgelegt werden.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

var loadOpts = new aspose.threed.Discreet3dsLoadOptions();

// Legt fest, ob die in der ersten Frame der Animation Track definierte Transformation verwendet werden soll.
loadOpts.setApplyAnimationTransform(true);

// Koordinatensystem umkehren
loadOpts.setFlipCoordinateSystem(true);

// Bevorzugt die Verwendung von Gamma-korrigierter Farbe, wenn eine 3ds-Datei sowohl die ursprüngliche Farbe als auch die Gamma-korrigierte Farbe bereitstellt.
loadOpts.setGammaCorrectedColor(true);

{{< /highlight >}}

### **Verwendung der Obj-Ladeoptionen**
Der folgende Code zeigt, wie Ladeoptionen vor dem Laden einer 3D-Obj-Datei festgelegt werden.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

var loadObjOpts  = new aspose.threed.ObjLoadOptions();

// Materialien aus externer Materialbibliothek importieren
loadObjOpts.setEnableMaterials(true);

// Koordinatensystem umkehren.
loadObjOpts.setFlipCoordinateSystem(true);

{{< /highlight >}}

### **Verwendung der STL-Ladeoptionen**
Der folgende Code zeigt, wie Ladeoptionen vor dem Laden einer STL-Datei festgelegt werden.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Initialisiere ein Objekt
var loadSTLOpts   = new aspose.threed.StlLoadOptions();

// Koordinatensystem umkehren.
loadSTLOpts.setFlipCoordinateSystem(true);

{{< /highlight >}}

### **Verwendung der U3D-Ladeoptionen**
Der folgende Code zeigt, wie Ladeoptionen vor dem Laden einer U3D-Datei festgelegt werden.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Initialisiere ein Objekt
var loadU3DOpts = new aspose.threed.U3dLoadOptions();

// Koordinatensystem umkehren.
loadU3DOpts.setFlipCoordinateSystem(true);

{{< /highlight >}}

### **Verwendung der glTF-Ladeoptionen**
Der folgende Code zeigt, wie Ladeoptionen vor dem Laden einer glTF-Datei festgelegt werden.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Ladeoptionen festlegen
var loadOpt = new aspose.threed.GltfLoadOptions();

// Der Standardwert ist true, normalerweise müssen wir ihn nicht ändern. Aspose.3D kehrt während des Ladens und Speicherns automatisch die V/T-Texturkoordinate um.
loadOpt.setFlipTexCoordV(true);

{{< /highlight >}}

### **Verwendung der Ply-Ladeoptionen**
Der folgende Code zeigt, wie Ladeoptionen vor dem Laden eines PLY-Modells festgelegt werden.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Initialisiere Scene-Klassenobjekt
var scene = new aspose.threed.Scene();

// Initialisiere ein Objekt
var loadPLYOpts  = new aspose.threed.PlyLoadOptions();

// Koordinatensystem umkehren.
loadPLYOpts.setFlipCoordinateSystem(true);

// 3D-Ply-Modell laden
scene.open("vase-v2.ply", loadPLYOpts);

{{< /highlight >}}

### **Verwendung der DirectX X-Ladeoptionen**
Der folgende Code zeigt, wie Ladeoptionen vor dem Laden einer DirectX X-Datei festgelegt werden.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Initialisiere Scene-Klassenobjekt
var scene = new aspose.threed.Scene();

// Initialisiere ein Objekt
var loadXOpts = new aspose.threed.XLoadOptions(aspose.threed.FileContentType.ASCII);

// Koordinatensystem umkehren.
loadXOpts.setFlipCoordinateSystem(true);

// 3D-X-Datei laden
scene.open("warrior.x", loadXOpts);

{{< /highlight >}}

### **Verwendung von FBX-Ladeoptionen**

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

//Dies gibt alle in GlobalSettings in FBX-Datei definierten Eigenschaften aus.
var opt = new aspose.threed.FbxLoadOptions();

opt.setKeepBuiltinGlobalSettings(true);

{{< /highlight >}}