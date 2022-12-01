---
title: Manipulera anpassade egenskaper för en 3D Scene
type: docs
weight: 80
url: /sv/net/manipulate-custom-properties-of-a-3d-scene/
description: Utvecklare kan Lägga till, hämta och ta bort anpassade egenskaper för 3D objekt. Ta bortProperty, HämtaProperty, SetProperty medlemmar i 3D objekt är en uppsättning korthändede metoder för att manipulera anpassade egenskaper Objekt.
---
## **Lägg till, hämta och ta bort anpassade egenskaper för en 3D Objekt**
Utvecklare kan Lägga till, hämta och ta bort anpassade egenskaper för 3D objekt. `RemoveProperty`, `GetProperty`, `SetProperty` medlemmar av 3D föremål är en uppsättning korthändiga metoder för att manipulera skräddarsydda egenskaper av den Objekt. Det här är kodexemplet för att ange, hämta och ta bort en egenskap:

**C#**

{{< highlight "java" >}}

 // initialize a scene 

Scene scene = new Scene();

// create a Box instance

var box = scene.RootNode.CreateChildNode("box", new Box());

// add custom property

box.SetProperty("property-name", "property-value");

box.SetProperty("property-name2", "property-value2");

// get a custom property by name

Property property = (Property)box.GetProperty("property-name");

// remove the custom property by name or property instance

box.RemoveProperty("property-name");

box.RemoveProperty(property);

// save 3D scene

scene.Save("test.fbx", FileFormat.FBX7400ASCII);

scene.Save("test.gltf", new GLTFSaveOptions(FileFormat.GLTF){SaveExtras = true});

scene.Save("test-2.gltf", new GLTFSaveOptions(FileFormat.GLTF2){SaveExtras = true});

{{< /highlight >}}

{{% alert color="primary" %}} 

För att spara anpassade egenskaper i GLTF-modellerna måste du ställa in SaveExtras till true. Standardvärdet på egenskapen SaveExtras är falskt.

{{% /alert %}}
