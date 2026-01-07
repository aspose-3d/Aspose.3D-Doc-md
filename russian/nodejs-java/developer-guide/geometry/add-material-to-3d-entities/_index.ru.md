---
title: "Добавить материал к 3D-объектам"
type: docs
weight: 60
url: "/ru/nodejs-java/add-material-to-3d-entities/"
description: "PBR играет ключевую роль в визуализации игрового движка, обеспечивая эффективную и реалистичную отрисовку взаимодействия света и поверхности посредством ослабления яркости и рассеивания отраженного света. Разработчики могут использовать API Aspose.3D для применения PBR-материала к 3D-объектам в сцене. Этот пример кода демонстрирует, как создать объект Box и затем применить PBR-материал."
---

{{% alert color="primary" %}}

PBR играет ключевую роль в визуализации игрового движка, обеспечивая эффективную и реалистичную визуализацию взаимодействия света и поверхности посредством ослабления яркости и рассеивания отраженного света. Разработчики могут использовать API Aspose.3D для применения PBR-материала к 3D-объектам в сцене. Этот пример кода демонстрирует, как создать объект Box, а затем применить к нему PBR-материал.

{{% /alert %}}


## **Применение Physically Based Rendering (PBR) Материала к Box**

{{< highlight java >}}

var aspose = aspose || {};

aspose.threed = require("aspose.3d");

// инициализация сцены
var scene = new aspose.threed.Scene();

// инициализация объекта PbrMaterial
var mat = new aspose.threed.PbrMaterial();

// почти металлический материал
mat.setMetallicFactor(0.9);

// поверхность материала очень шероховатая
mat.setRoughnessFactor(0.9);

// создание Box, к которому будет применен материал
var boxNode = scene.getRootNode().createChildNode("box", new aspose.threed.Box());
boxNode.setMaterial(mat);

// сохранение 3D-сцены в формате USDZ
scene.save("PBR_Material_Box_Out.usdz");

{{< /highlight >}}