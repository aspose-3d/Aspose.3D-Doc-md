---
title: Añadir Material a Entidades 3D
type: docs
weight: 60
url: "/es/nodejs-java/add-material-to-3d-entities/"
description: PBR juega un papel clave para los visuales del motor de juego, con su renderizado eficiente y realista de las interacciones entre la luz y la superficie a través de la atenuación del brillo y la dispersión de la luz reflejada. Los desarrolladores pueden usar la API de Aspose.3D para aplicar un material PBR a objetos 3D en una escena. Este ejemplo de código demuestra cómo crear un objeto Box y luego aplicar el material PBR.
---

{{% alert color="primary" %}}

PBR juega un papel clave para los visuales del motor de juego, con su renderizado eficiente y realista de las interacciones entre la luz y la superficie a través de la atenuación del brillo y la dispersión de la luz reflejada. Los desarrolladores pueden usar la API Aspose.3D para aplicar un material PBR a objetos 3D en una escena. Este ejemplo de código demuestra cómo crear un objeto Box y luego aplicar el material PBR.

{{% /alert %}}


## **Aplicar Material de Renderizado Basado en la Física (PBR) a un Box**

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// inicializar una escena
var scene = new aspose.threed.Scene();

// inicializar objeto de material PBR
var mat = new aspose.threed.PbrMaterial();

// un material casi metálico
mat.setMetallicFactor(0.9);

// la superficie del material es muy rugosa
mat.setRoughnessFactor(0.9);

// crear un box al que se aplicará el material
var boxNode = scene.getRootNode().createChildNode("box", new aspose.threed.Box());
boxNode.setMaterial(mat);

// guardar la escena 3D en formato USDZ
scene.save("PBR_Material_Box_Out.usdz");

{{< /highlight >}}