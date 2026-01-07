---
title: "Lavorare con l'Estrusione Lineare"
type: docs
weight: 80
url: "/it/nodejs-java/working-with-linear-extrusion/"
description: Aspose.3D per Node.js via Java offre la classe LinearExtrusion, che accetta una forma 2D come input ed estende la forma nella terza dimensione.
---

# **Esecuzione dell'Estrusione Lineare**
Aspose.3D for Node.js via Java offre la classe `LinearExtrusion` che prende una forma 2D come input ed estende la forma nella terza dimensione. Il seguente frammento di codice mostra come eseguire l'estrusione lineare:

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Inizializza la forma di base da estrudere
// Inizializza il profilo di base da estrudere
var profile=new aspose.threed.RectangleShape();
profile.setRoundingRadius(0.3);

// Esegui l'estrusione lineare passando una forma 2D come input ed estendendo la forma nella terza dimensione
var extrusion =new aspose.threed.LinearExtrusion(profile, 10);
extrusion.setSlices(100);
extrusion.setCenter(true);
extrusion.setTwist(360);
extrusion.setTwistOffset(new aspose.threed.Vector3(10, 0, 0));

// Crea una scena
var scene = new aspose.threed.Scene();

// Crea un nodo figlio passando l'estrusione
scene.getRootNode().createChildNode(extrusion);

// Salva la scena 3D
scene.save("LinearExtrusion.obj");

{{< /highlight >}}

# **Sezioni nell'Estrusione Lineare**
Aspose.3D for Node.js via Java offre il metodo `setSlices()` della classe `LinearExtrusion`. Il metodo setSlices() definisce il numero di punti intermedi lungo il percorso dell'estrusione. Il seguente frammento di codice mostra come utilizzare il metodo setSlices() nell'estrusione lineare:

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Inizializza il profilo di base da estrudere
var profile=new aspose.threed.RectangleShape();
profile.setRoundingRadius(0.3);

// Crea una scena
var scene = new aspose.threed.Scene();

// Crea nodo sinistro
var left=scene.getRootNode().createChildNode();
// Crea nodo destro
var right=scene.getRootNode().createChildNode();
left.getTransform().setTranslation(new aspose.threed.Vector3(5, 0, 0));

// Il parametro Sezioni definisce il numero di punti intermedi lungo il percorso dell'estrusione
// Esegui l'estrusione lineare sul nodo sinistro utilizzando la proprietà sezioni
var extrusion1 =new aspose.threed.LinearExtrusion(profile, 2);
extrusion1.setSlices(2);
left.createChildNode(extrusion1);

// Esegui l'estrusione lineare sul nodo destro utilizzando la proprietà sezioni
var extrusion2 =new aspose.threed.LinearExtrusion(profile, 2);
extrusion2.setSlices(10);
right.createChildNode(extrusion2);

// Salva la scena 3D
scene.save("SlicesInLinearExtrusion.obj");

{{< /highlight >}}

# **Centro nell'Estrusione Lineare**
Aspose.3D for Node.js via Java offre il metodo `setCenter()` della classe `LinearExtrusion`. Se il metodo setCenter() è impostato su true, l'intervallo di estrusione va da -Altezza/2 a Altezza/2, altrimenti, l'estrusione va da 0 a Altezza. Il seguente frammento di codice mostra come utilizzare il metodo setCenter() nell'estrusione lineare:

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Inizializza il profilo di base da estrudere
var profile=new aspose.threed.RectangleShape();
profile.setRoundingRadius(0.3);

// Crea una scena
var scene = new aspose.threed.Scene();

// Crea nodo sinistro
var left=scene.getRootNode().createChildNode();
// Crea nodo destro
var right=scene.getRootNode().createChildNode();
left.getTransform().setTranslation(new aspose.threed.Vector3(5, 0, 0));

// Imposta il piano di riferimento
var box=new aspose.threed.Box(0.01, 3, 3);

// Se la proprietà Center è true, l'intervallo di estrusione va da -Altezza/2 a Altezza/2, altrimenti l'estrusione va da 0 a Altezza
// Esegui l'estrusione lineare sul nodo sinistro utilizzando le proprietà center e sezioni
var extrusion1 =new aspose.threed.LinearExtrusion(profile, 2);
extrusion1.setSlices(3);
extrusion1.setCenter(false);
left.createChildNode(extrusion1);
left.createChildNode(box);

// Esegui l'estrusione lineare sul nodo destro utilizzando le proprietà center e sezioni
var extrusion2 =new aspose.threed.LinearExtrusion(profile, 2);
extrusion2.setSlices(3);
extrusion2.setCenter(true);
right.createChildNode(extrusion2);
right.createChildNode(box);

// Salva la scena 3D
scene.save("CenterInLinearExtrusion.obj");

{{< /highlight >}}

# **Rotazione nell'Estrusione Lineare**
Aspose.3D for Node.js via Java offre il metodo `setTwist()` della classe `LinearExtrusion`. Il metodo setTwist() gestisce il grado di rotazione durante l'estrusione della forma. Il seguente frammento di codice mostra come utilizzare il metodo setTwist() nell'estrusione lineare:

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Inizializza il profilo di base da estrudere
var profile=new aspose.threed.RectangleShape();
profile.setRoundingRadius(0.3);

// Crea una scena
var scene = new aspose.threed.Scene();

// Crea nodo sinistro
var left=scene.getRootNode().createChildNode();
// Crea nodo destro
var right=scene.getRootNode().createChildNode();
left.getTransform().setTranslation(new aspose.threed.Vector3(5, 0, 0));

// La proprietà Rotazione definisce il grado di rotazione durante l'estrusione della forma
// Esegui l'estrusione lineare sul nodo sinistro utilizzando la proprietà sezioni
var extrusion1 =new aspose.threed.LinearExtrusion(profile, 10);
extrusion1.setSlices(100);
extrusion1.setTwist(360);
left.createChildNode(extrusion1);

// Esegui l'estrusione lineare sul nodo destro utilizzando la proprietà rotazione
var extrusion2 =new aspose.threed.LinearExtrusion(profile, 10);
extrusion2.setSlices(100);
extrusion2.setTwist(360);
right.createChildNode(extrusion2);

// Salva la scena 3D
scene.save("DirectionInLinearExtrusion.obj");


{{< /highlight >}}

# **Offset di Rotazione nell'Estrusione Lineare**
Aspose.3D for Node.js via Java offre il metodo `setTwistOffset()` della classe `LinearExtrusion`. Il metodo setTwistOffset() definisce l'offset di rotazione durante l'estrusione della forma. Il seguente frammento di codice mostra come utilizzare il metodo setTwistOffset() nell'estrusione lineare:

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Inizializza il profilo di base da estrudere
var profile=new aspose.threed.RectangleShape();
profile.setRoundingRadius(0.3);

// Crea una scena
var scene = new aspose.threed.Scene();

// Crea nodo sinistro
var left=scene.getRootNode().createChildNode();
// Crea nodo destro
var right=scene.getRootNode().createChildNode();
left.getTransform().setTranslation(new aspose.threed.Vector3(5, 0, 0));

// La proprietà Offset di Rotazione definisce l'offset di rotazione durante l'estrusione della forma
// Esegui l'estrusione lineare sul nodo sinistro utilizzando la proprietà sezioni
var extrusion1 =new aspose.threed.LinearExtrusion(profile, 10);
extrusion1.setSlices(100);
extrusion1.setTwist(360);
left.createChildNode(extrusion1);

// Esegui l'estrusione lineare sul nodo destro utilizzando la proprietà rotazione, offset di rotazione e sezioni
var extrusion2 =new aspose.threed.LinearExtrusion(profile, 10);
extrusion2.setSlices(100);
extrusion2.setTwist(360);
extrusion2.setTwistOffset(new aspose.threed.Vector3(3, 0, 0));
right.createChildNode(extrusion2);

// Salva la scena 3D
scene.save("TwistOffsetInLinearExtrusion.obj");

{{< /highlight >}}

# **Direzione nell'Estrusione Lineare**
Aspose.3D for Node.js via Java offre il metodo `setDirection()` della classe `LinearExtrusion`. Il metodo setDirection() definisce la direzione dell'estrusione. Il seguente frammento di codice mostra come utilizzare il metodo setDirection() nell'estrusione lineare:

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Inizializza il profilo di base da estrudere
var profile=new aspose.threed.RectangleShape();
profile.setRoundingRadius(0.3);

// Crea una scena
var scene = new aspose.threed.Scene();

// Crea nodo sinistro
var left=scene.getRootNode().createChildNode();
// Crea nodo destro
var right=scene.getRootNode().createChildNode();
left.getTransform().setTranslation(new aspose.threed.Vector3(5, 0, 0));

// La proprietà Direzione definisce la direzione dell'estrusione
// Esegui l'estrusione lineare sul nodo sinistro utilizzando la proprietà sezioni
var extrusion1 =new aspose.threed.LinearExtrusion(profile, 10);
extrusion1.setSlices(100);
extrusion1.setTwist(360);
left.createChildNode(extrusion1);

// Esegui l'estrusione lineare sul nodo destro utilizzando la proprietà rotazione, offset di rotazione e sezioni
var extrusion2 =new aspose.threed.LinearExtrusion(profile, 10);
extrusion2.setSlices(100);
extrusion2.setTwist(360);
extrusion2.setDirection(new aspose.threed.Vector3(0.3, 0.2, 1));
right.createChildNode(extrusion2);

// Salva la scena 3D
scene.save("DirectionInLinearExtrusion.obj");

{{< /highlight >}}