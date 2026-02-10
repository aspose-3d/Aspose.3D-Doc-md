---
title: Skapa ett tomt 3D-dokument
type: docs
weight: 20
url: /sv/java/create-an-empty-3d-document/
description: Aspose. 3D for Java API har stöd för att skapa 3D scen från början, och spara sedan i stödt 3D format.
---
##  **Skapa en tom 3D Scene och spara i format som stöds 3D**
Aspose. 3D for Java API har stöd för att skapa 3D scen från början, och spara sedan i stödt 3D format.
###  **Skapa en tom 3D Scene**
Please follow these steps to create a 3D Scene with Aspose.3D for Java API:

1. Skapa en instans i**Scene**Klass som representerar 3D scen.
1. Skapa 3D-dokumentet genom att ringa**Spara**Metoden**Scene**Klasseinstans.
####  **Skapa en tom 3D Scene: Programmeringsprovning**
{{< highlight "java" >}}
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
MyDir = MyDir + "document.fbx";
// Create an object of the Scene class
Scene scene = new Scene();
// Save 3D scene document
scene.save(MyDir, FileFormat.FBX7500ASCII);
{{< /highlight >}}




