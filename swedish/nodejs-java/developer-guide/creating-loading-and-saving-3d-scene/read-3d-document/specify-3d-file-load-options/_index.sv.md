---
title: "Ange alternativ för inläsning av 3D-filer"
type: docs
weight: 10
url: "/sv/nodejs-java/specify-3d-file-load-options/"
description: Det finns flera överbelastningar för metoden Scene.open eller konstruktörsöverbelastningar för klassen Scene som accepterar en instans av LoadOptions.
---

## **3D Filalternativ för inläsning**
Det finns flera Scene.open metodöverbelastningar eller Scene konstruktoröverbelastningar som accepterar LoadOptions instans. Detta bör vara en instans av en klass som är härledd från LoadOptions klassen. Varje filformat har en motsvarande klass som håller inläsningsalternativ för det filformatet, till exempel finns det ColladaSaveOptions för FileFormat.COLLADA spara format.
### **Användning av Discreet 3DS Inläsningsalternativ**
Koden nedan visar hur man ställer in inläsningsalternativ innan en Discreet 3DS fil läses in.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

var loadOpts = new aspose.threed.Discreet3dsLoadOptions();

// Ställer in om transformationen som definieras i det första animeringsspåret ska användas.
loadOpts.setApplyAnimationTransform(true);

// Vänd koordinatsystemet
loadOpts.setFlipCoordinateSystem(true);

// Föredrar att använda gamma-korrigerad färg om en 3ds fil tillhandahåller både originalfärg och gamma-korrigerad färg.
loadOpts.setGammaCorrectedColor(true);

{{< /highlight >}}

### **Användning av Obj Inläsningsalternativ**
Koden nedan visar hur man ställer in inläsningsalternativ innan en 3D Obj fil läses in.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

var loadObjOpts  = new aspose.threed.ObjLoadOptions();

// Importera material från externt materialbiblioteksfil
loadObjOpts.setEnableMaterials(true);

// Vänd koordinatsystemet.
loadObjOpts.setFlipCoordinateSystem(true);

{{< /highlight >}}

### **Användning av STL Inläsningsalternativ**
Koden nedan visar hur man ställer in inläsningsalternativ innan en STL fil läses in.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// Initiera ett objekt
var loadSTLOpts   = new aspose.threed.StlLoadOptions();

// Vänd koordinatsystemet.
loadSTLOpts.setFlipCoordinateSystem(true);

{{< /highlight >}}

### **Användning av U3D Inläsningsalternativ**
Koden nedan visar hur man ställer in inläsningsalternativ innan en U3D fil läses in.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// Initiera ett objekt
var loadU3DOpts = new aspose.threed.U3dLoadOptions();

// Vänd koordinatsystemet.
loadU3DOpts.setFlipCoordinateSystem(true);

{{< /highlight >}}

### **Användning av glTF Inläsningsalternativ**
Koden nedan visar hur man ställer in inläsningsalternativ innan en glTF fil läses in.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// Ställ in inläsningsalternativ
var loadOpt = new aspose.threed.GltfLoadOptions();

// Standardvärdet är sant, vanligtvis behöver vi inte ändra det. Aspose.3D kommer automatiskt att vända V/T texturkoordinaten under inläsning och sparning.
loadOpt.setFlipTexCoordV(true);

{{< /highlight >}}

### **Användning av Ply Inläsningsalternativ**
Koden nedan visar hur man ställer in inläsningsalternativ innan en PLY modell läses in.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// initiera Scene klass objekt
var scene = new aspose.threed.Scene();

// initiera ett objekt
var loadPLYOpts  = new aspose.threed.PlyLoadOptions();

// Vänd koordinatsystemet.
loadPLYOpts.setFlipCoordinateSystem(true);

// läs in 3D Ply modell
scene.open("vase-v2.ply", loadPLYOpts);

{{< /highlight >}}

### **Användning av DirectX X Inläsningsalternativ**
Koden nedan visar hur man ställer in inläsningsalternativ innan en DirectX X fil läses in.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// initiera Scene klass objekt
var scene = new aspose.threed.Scene();

// initiera ett objekt
var loadXOpts = new aspose.threed.XLoadOptions(aspose.threed.FileContentType.ASCII);

// vänd koordinatsystemet.
loadXOpts.setFlipCoordinateSystem(true);

// läs in 3D X fil
scene.open("warrior.x", loadXOpts);

{{< /highlight >}}

### **Använd FBX Inläsningsalternativ**

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

//Detta kommer att skriva ut alla egenskaper som definierats i GlobalSettings i FBX fil.
var opt = new aspose.threed.FbxLoadOptions();

opt.setKeepBuiltinGlobalSettings(true);

{{< /highlight >}}