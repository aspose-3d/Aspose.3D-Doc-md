---
title: Spécifier les options de chargement des fichiers 3D
type: docs
weight: 10
url: "/fr/nodejs-java/specify-3d-file-load-options/"
description: Il existe plusieurs surcharge de la méthode open de la classe Scene ou surcharge du constructeur de la classe Scene qui acceptent une instance de LoadOptions.
---

## **3D File Load Options**
Il existe plusieurs méthodes de surcharge de Scene.open ou de surcharge du constructeur de la classe Scene qui acceptent une instance de LoadOptions. Il s'agit d'une instance d'une classe dérivée de la classe LoadOptions. Chaque format de chargement possède une classe correspondante qui contient les options de chargement pour ce format de chargement, par exemple, il existe ColladaSaveOptions pour le format de sauvegarde FileFormat.COLLADA.
### **Utilisation des options de chargement Discreet 3DS**
Le code ci-dessous montre comment définir les options de chargement avant de charger un fichier Discreet 3DS.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

var loadOpts = new aspose.threed.Discreet3dsLoadOptions();

// Définit si la transformation définie dans la première image de la piste d'animation doit être utilisée.
loadOpts.setApplyAnimationTransform(true);

// Inverse le système de coordonnées
loadOpts.setFlipCoordinateSystem(true);

// Préférez utiliser la couleur corrigée gamma si un fichier 3ds fournit à la fois la couleur originale et la couleur corrigée gamma.
loadOpts.setGammaCorrectedColor(true);

{{< /highlight >}}

### **Utilisation des options de chargement Obj**
Le code ci-dessous montre comment définir les options de chargement avant de charger un fichier 3D Obj.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

var loadObjOpts  = new aspose.threed.ObjLoadOptions();

// Importe les matériaux à partir d'un fichier de bibliothèque de matériaux externe
loadObjOpts.setEnableMaterials(true);

// Inverse le système de coordonnées.
loadObjOpts.setFlipCoordinateSystem(true);

{{< /highlight >}}

### **Utilisation des options de chargement STL**
Le code ci-dessous montre comment définir les options de chargement avant de charger un fichier STL.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// Initialise un objet
var loadSTLOpts   = new aspose.threed.StlLoadOptions();

// Inverse le système de coordonnées.
loadSTLOpts.setFlipCoordinateSystem(true);

{{< /highlight >}}

### **Utilisation des options de chargement U3D**
Le code ci-dessous montre comment définir les options de chargement avant de charger un fichier U3D.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// Initialise un objet
var loadU3DOpts = new aspose.threed.U3dLoadOptions();

// Inverse le système de coordonnées.
loadU3DOpts.setFlipCoordinateSystem(true);

{{< /highlight >}}

### **Utilisation des options de chargement glTF**
Le code ci-dessous montre comment définir les options de chargement avant de charger un fichier glTF.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// Définir les options de chargement
var loadOpt = new aspose.threed.GltfLoadOptions();

// La valeur par défaut est true, nous n'avons généralement pas besoin de la modifier. Aspose.3D inversera automatiquement la coordonnée V/T de la texture pendant le chargement et la sauvegarde.
loadOpt.setFlipTexCoordV(true);

{{< /highlight >}}

### **Utilisation des options de chargement Ply**
Le code ci-dessous montre comment définir les options de chargement avant de charger un modèle PLY.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// initialise l'objet de classe Scene
var scene = new aspose.threed.Scene();

// initialise un objet
var loadPLYOpts  = new aspose.threed.PlyLoadOptions();

// Inverse le système de coordonnées.
loadPLYOpts.setFlipCoordinateSystem(true);

// charge le modèle 3D Ply
scene.open("vase-v2.ply", loadPLYOpts);

{{< /highlight >}}

### **Utilisation des options de chargement DirectX X**
Le code ci-dessous montre comment définir les options de chargement avant de charger un fichier DirectX X.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

// initialise l'objet de classe Scene
var scene = new aspose.threed.Scene();

// initialise un objet
var loadXOpts = new aspose.threed.XLoadOptions(aspose.threed.FileContentType.ASCII);

// inverse le système de coordonnées.
loadXOpts.setFlipCoordinateSystem(true);

// charge le fichier 3D X
scene.open("warrior.x", loadXOpts);

{{< /highlight >}}

### **Utilisation des options de chargement FBX**

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.threed");

//Ceci affichera toutes les propriétés définies dans GlobalSettings dans le fichier FBX.
var opt = new aspose.threed.FbxLoadOptions();

opt.setKeepBuiltinGlobalSettings(true);

{{< /highlight >}}