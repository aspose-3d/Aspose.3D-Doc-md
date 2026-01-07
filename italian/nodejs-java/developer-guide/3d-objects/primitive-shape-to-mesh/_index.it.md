---
title: Forma primitiva a mesh
type: docs
weight: 20
url: "/it/nodejs-java/primitive-shape-to-mesh/"
description: Aspose.3D per Node.js tramite API Java supporta la conversione di qualsiasi forma primitiva in mesh. Le forme primitive includono gli oggetti più basilari e utilizzati come scatola, sfera, piano, cilindro e toro.
---

## **Converti una forma primitiva in mesh**
Aspose.3D per Node.js via Java API offre il supporto per convertire qualsiasi forma primitiva in mesh. Le forme primitive includono gli oggetti più basilari e utilizzati come scatola, sfera, piano, cilindro e toro.

{{% alert color="primary" %}}

Qualsiasi classe che implementa un'interfaccia IMeshConvertible può essere convertita in mesh durante l'esportazione in qualsiasi formato di file 3D.

{{% /alert %}}
### **Converti una sfera primitiva in mesh**
Una sfera è un oggetto geometrico perfettamente rotondo nello spazio tridimensionale che appare ovunque, dalle palle sportive ai pianeti nello spazio. Utilizziamo la primitiva Sfera per creare una mesh.
L'esempio di codice seguente converte una Sfera in mesh.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Inizializza oggetto tramite classe Sfera
var convertible = new aspose.threed.Sphere();

// Converti una Sfera in Mesh
var mesh = convertible.toMesh();

{{< /highlight >}}

### **Converti una scatola in mesh**
Una Scatola descrive una varietà di contenitori e recipienti per uso permanente come stoccaggio o per uso temporaneo, spesso per il trasporto di contenuti. Utilizziamo la primitiva Scatola per creare una mesh. L'esempio di codice seguente converte una Scatola in mesh.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Inizializza oggetto tramite classe Scatola
var convertible = new aspose.threed.Box();

// Converti una Scatola in Mesh
var mesh = convertible.toMesh();

{{< /highlight >}}

### **Converti un piano in mesh**
Un piano si estende infinitamente senza spessore. Un esempio di piano è un piano di coordinate. Utilizziamo la primitiva Piano per creare una mesh. L'esempio di codice seguente converte un Piano in mesh.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Inizializza oggetto tramite classe Piano
var convertible = new aspose.threed.Plane();

// Converti un Piano in Mesh
var mesh = convertible.toMesh();

{{< /highlight >}}

### **Converti un cilindro in mesh**
Un cilindro è una delle forme geometriche curvilinee più basilari, la superficie formata dai punti a una distanza fissa da una data linea retta, l'asse del cilindro. Può essere utilizzato in molti posti, ad esempio come pilastro di fronte a una casa o come albero di trasmissione di un'auto. Utilizziamo la primitiva Cilindro per creare una mesh. L'esempio di codice seguente converte un Cilindro in mesh.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Inizializza oggetto tramite classe Cilindro
var convertible = new aspose.threed.Cylinder();

// Converti un Cilindro in Mesh
var mesh = convertible.toMesh();

{{< /highlight >}}

### **Converti un toro in mesh**
Un toro è una superficie di rivoluzione generata facendo ruotare un cerchio nello spazio tridimensionale attorno a un asse coplanare con il cerchio. Se l'asse di rivoluzione non tocca il cerchio, la superficie ha una forma ad anello ed è chiamata toro di rivoluzione. Utilizziamo la primitiva Toro per creare una mesh. L'esempio di codice seguente converte un Toro in mesh.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Inizializza oggetto tramite classe Toro
var convertible = new aspose.threed.Torus();

// Converti un Toro in Mesh
var mesh = convertible.toMesh();

{{< /highlight >}}