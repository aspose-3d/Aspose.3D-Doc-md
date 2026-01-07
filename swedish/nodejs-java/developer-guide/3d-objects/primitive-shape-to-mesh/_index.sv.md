---
title: Primitiv form till nät
type: docs
weight: 20
url: "/sv/nodejs-java/primitive-shape-to-mesh/"
description: Aspose.3D för Node.js via Java API har stöd för att konvertera alla primitiva former till mesh. Primitiva former inkluderar de mest grundläggande och använda objekten som kub, sfär, plan, cylinder och torus.
---

## **Konvertera Primitiv Form till Nät**
Aspose.3D för Node.js via Java API har stöd för att konvertera vilken primitiv form som helst till nät. Primitiva former inkluderar de mest grundläggande och använda objekten som låda, sfär, plan, cylinder och torus.

{{% alert color="primary" %}}

Varje klass som implementerar ett gränssnitt IMeshConvertible kan konverteras till nät vid export till ett 3D-filformat.

{{% /alert %}}
### **Konvertera Sfär Primitiv till Nät**
En sfär är ett perfekt runt geometriskt objekt i tredimensionellt utrymme som finns överallt från sportbollar till planeter i rymden. Låt oss använda den primitiva formen Sfär för att skapa ett nät.
Exempelkoden nedan konverterar en Sfär till ett nät.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Initiera objekt med Sfär-klassen
var convertible = new aspose.threed.Sphere();

// Konvertera en Sfär till ett nät
var mesh = convertible.toMesh();

{{< /highlight >}}

### **Konvertera Låda till Nät**
En Låda beskriver en mängd olika behållare och uppställningar för permanent användning som förvaring, eller för tillfällig användning, ofta för att transportera innehåll. Låt oss använda den primitiva formen Låda för att skapa ett nät. Exempelkoden nedan konverterar en Låda till ett nät.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Initiera objekt med Låda-klassen
var convertible = new aspose.threed.Box();

// Konvertera en Låda till ett nät
var mesh = convertible.toMesh();

{{< /highlight >}}

### **Konvertera ett Plan till Nät**
Ett plan sträcker sig oändligt utan tjocklek. Ett exempel på ett plan är ett koordinatplan. Låt oss använda den primitiva formen Plan för att skapa ett nät. Exempelkoden nedan konverterar ett Plan till ett nät.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Initiera objekt med Plan-klassen
var convertible = new aspose.threed.Plane();

// Konvertera ett Plan till ett nät
var mesh = convertible.toMesh();

{{< /highlight >}}

### **Konvertera en Cylinder till Nät**
En cylinder är en av de mest grundläggande krökta geometriska formerna, ytan som bildas av punkter på ett fast avstånd från en given rak linje, cylinderns axel. Den kan användas på många platser, till exempel som en pelare framför ett hem eller som en bil drivaxel. Låt oss använda den primitiva formen Cylinder för att skapa ett nät. Exempelkoden nedan konverterar en Cylinder till ett nät.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Initiera objekt med Cylinder-klassen
var convertible = new aspose.threed.Cylinder();

// Konvertera en Cylinder till ett nät
var mesh = convertible.toMesh();

{{< /highlight >}}

### **Konvertera en Torus till Nät**
En torus är en revolutioneringsyta som genereras genom att rotera en cirkel i tredimensionellt utrymme kring en axel som ligger i samma plan som cirkeln. Om rotationsaxeln inte rör cirkeln har ytan en ringform och kallas en revolutionstoroid. Låt oss använda den primitiva formen Torus för att skapa ett nät. Exempelkoden nedan konverterar en Torus till ett nät.

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// Initiera objekt med Torus-klassen
var convertible = new aspose.threed.Torus();

// Konvertera en Torus till ett nät
var mesh = convertible.toMesh();

{{< /highlight >}}