---
title: Specifica le opzioni di caricamento dei file 3D
type: docs
weight: 10
url: "/it/nodejs-java/specify-3d-file-load-options/"
description: "Ci sono diversi overload del metodo Scene.open o overload del costruttore della classe Scene che accettano un'istanza di LoadOptions."
---

## **3D File Load Options**
Ci sono diversi overload del metodo Scene.open o overload del costruttore della classe Scene che accettano un'istanza di LoadOptions. Questa dovrebbe essere un'istanza di una classe derivata dalla classe LoadOptions. Ogni formato di caricamento ha una classe corrispondente che contiene le opzioni di caricamento per quel formato di caricamento, ad esempio c'è ColladaSaveOptions per il formato di salvataggio FileFormat.COLLADA.
### **Utilizzo delle opzioni di caricamento Discreet 3DS**
Il codice seguente mostra come impostare le opzioni di caricamento prima di caricare un file Discreet 3DS.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

var loadOpts = new aspose.threed.Discreet3dsLoadOptions();

// Imposta se utilizzare la trasformazione definita nel primo frame dell'animazione.
loadOpts.setApplyAnimationTransform(true);

// Inverti il sistema di coordinate
loadOpts.setFlipCoordinateSystem(true);

// Preferisci utilizzare il colore con correzione gamma se un file 3ds fornisce sia il colore originale che il colore con correzione gamma.
loadOpts.setGammaCorrectedColor(true);

{{< /highlight >}}

### **Utilizzo delle opzioni di caricamento Obj**
Il codice seguente mostra come impostare le opzioni di caricamento prima di caricare un file 3D Obj.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

var loadObjOpts  = new aspose.threed.ObjLoadOptions();

// Importa i materiali da un file di libreria dei materiali esterni
loadObjOpts.setEnableMaterials(true);

// Inverti il sistema di coordinate.
loadObjOpts.setFlipCoordinateSystem(true);

{{< /highlight >}}

### **Utilizzo delle opzioni di caricamento STL**
Il codice seguente mostra come impostare le opzioni di caricamento prima di caricare un file STL.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Inizializza un oggetto
var loadSTLOpts   = new aspose.threed.StlLoadOptions();

// Inverti il sistema di coordinate.
loadSTLOpts.setFlipCoordinateSystem(true);

{{< /highlight >}}

### **Utilizzo delle opzioni di caricamento U3D**
Il codice seguente mostra come impostare le opzioni di caricamento prima di caricare un file U3D.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Inizializza un oggetto
var loadU3DOpts = new aspose.threed.U3dLoadOptions();

// Inverti il sistema di coordinate.
loadU3DOpts.setFlipCoordinateSystem(true);

{{< /highlight >}}

### **Utilizzo delle opzioni di caricamento glTF**
Il codice seguente mostra come impostare le opzioni di caricamento prima di caricare un file glTF.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Imposta le opzioni di caricamento
var loadOpt = new aspose.threed.GltfLoadOptions();

// Il valore predefinito è true, di solito non è necessario modificarlo. Aspose.3D invertirà automaticamente la coordinata V/T della texture durante il caricamento e il salvataggio.
loadOpt.setFlipTexCoordV(true);

{{< /highlight >}}

### **Utilizzo delle opzioni di caricamento Ply**
Il codice seguente mostra come impostare le opzioni di caricamento prima di caricare un modello PLY.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// inizializza l'oggetto classe Scene
var scene = new aspose.threed.Scene();

// inizializza un oggetto
var loadPLYOpts  = new aspose.threed.PlyLoadOptions();

// Inverti il sistema di coordinate.
loadPLYOpts.setFlipCoordinateSystem(true);

// carica modello Ply 3D
scene.open("vase-v2.ply", loadPLYOpts);

{{< /highlight >}}

### **Utilizzo delle opzioni di caricamento DirectX X**
Il codice seguente mostra come impostare le opzioni di caricamento prima di caricare un file DirectX X.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// inizializza l'oggetto classe Scene
var scene = new aspose.threed.Scene();

// inizializza un oggetto
var loadXOpts = new aspose.threed.XLoadOptions(aspose.threed.FileContentType.ASCII);

// inverti il sistema di coordinate.
loadXOpts.setFlipCoordinateSystem(true);

// carica file 3D X
scene.open("warrior.x", loadXOpts);

{{< /highlight >}}

### **Utilizzo delle opzioni di caricamento FBX**

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

//Questo stamperà tutte le proprietà definite in GlobalSettings nel file FBX.
var opt = new aspose.threed.FbxLoadOptions();

opt.setKeepBuiltinGlobalSettings(true);

{{< /highlight >}}