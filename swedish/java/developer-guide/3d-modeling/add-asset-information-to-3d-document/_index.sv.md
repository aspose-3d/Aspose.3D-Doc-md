---
title: Lägg till information om tillgångar i 3D.
type: docs
weight: 10
url: /sv/java/add-asset-information-to-3d-document/
description: Metadata är strukturerad information som beskriver, förklarar, lokaliserar eller gör det lättare att hämta, använda eller hantera en informationsresurs. Aspose.3D for Java API har stöd för att definiera metadata för scenen.
---
##  **Lägg till information om tillgångar i 3D.**
Metadata är strukturerad information som beskriver, förklarar, lokaliserar eller gör det lättare att hämta, använda eller hantera en informationsresurs. Aspose.3D for Java API har stöd för att definiera metadata för scenen.
###  **Definiera en metadata för scenen**
3D visar tillverkar stora mängder av metadata och bildinformation. Metadata är en tillgång och en del av showen.

1. Initiera en 3D scen med `Scene` klass.
1. Ange program/verktygsnamn.
1. Ange ansökan/verktygsleverantörens namn.
1. Ställ in måttenhet.
1. Ange måttenhetsskalfaktor.
1. Spara 3D-scenen i det stödda filformatet.

I det här exemplet antar vi att scenen är skapad av ett CAD-verktyg som heter “Egypt” och det är designat av “Manualdesk”:

{{< highlight "java" >}}
// Initialize a 3D scene
Scene scene = new Scene();
// Set application/tool name
scene.getAssetInfo().setApplicationName("Egypt");
// Set application/tool vendor name
scene.getAssetInfo().setApplicationVendor("Manualdesk");
// We use ancient egyption measurement unit Pole
scene.getAssetInfo().setUnitName("pole");
// One Pole equals to 60cm
scene.getAssetInfo().setUnitScaleFactor(0.6);
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
MyDir = MyDir + RunExamples.getOutputFilePath("InformationToScene.fbx");
// Save scene to 3D supported file formats
scene.save(MyDir, FileFormat.FBX7500ASCII);
{{< /highlight >}}
