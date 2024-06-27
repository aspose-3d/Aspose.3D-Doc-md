---
title: Skapa ett tomt 3D-dokument
type: docs
weight: 20
url: /sv/nodejs-java/create-an-empty-3d-document/
description: Aspose.3D for Node.js via Java API har stöd för att skapa 3D scen från början, och spara sedan i format som stöds 3D.
---
##  **Skapa en tom 3D Scene och spara i format som stöds 3D**
Aspose.3D for Node.js via Java API har stöd för att skapa 3D scen från början, och spara sedan i format som stöds 3D.
###  **Skapa en tom 3D Scene**
Please follow these steps to create a 3D Scene with Aspose.3D for Node.js via Java API:

1. Skapa en instans i**Scene**Klass som representerar 3D scen.
1. Skapa 3D-dokumentet genom att ringa**Spara**Metoden**Scene**Klasseinstans.
####  **Skapa en tom 3D Scene: Programmeringsprovning**
{{< highlight "java" >}}

var file="document.fbx";

// Create an object of the Scene class
var scene = new aspose.threed.Scene();

// Save 3D scene document
scene.save(file);

{{< /highlight >}}




