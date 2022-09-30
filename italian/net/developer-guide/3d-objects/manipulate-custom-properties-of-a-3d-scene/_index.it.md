---
title: Manipolare le proprietà personalizzate di una scena 3D
type: docs
weight: 80
url: /it/net/manipulate-custom-properties-of-a-3d-scene/
description: Gli sviluppatori possono aggiungere, recuperare e rimuovere proprietà personalizzate di 3D oggetti. I membri RemoveProperty, GetProperty, SetProperty di 3D oggetti sono un insieme di metodi a corto raggio per manipolare le proprietà personalizzate dell'oggetto.
---
## **Aggiungere, recuperare e rimuovere le proprietà personalizzate di un oggetto 3D**
Gli sviluppatori possono aggiungere, recuperare e rimuovere proprietà personalizzate di 3D oggetti. `RemoveProperty`, `GetProperty`, `SetProperty` i membri di 3D oggetti sono un insieme di metodi a corto raggio per manipolare le proprietà personalizzate dell'oggetto. Questo è l'esempio di codice per impostare, recuperare e rimuovere una proprietà personalizzata:

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

Per salvare le proprietà personalizzate nei modelli GLTF, è necessario impostare SaveExtras su true. Il valore predefinito della proprietà SaveExtras è falso.

{{% /alert %}}
