---
title: Lavorare con il raggio della sfera
type: docs
weight: 110
url: /it/net/working-with-radius-of-sphere/
description: Utilizzando Aspose.3D for .NET, puoi impostare il raggio di utilizzo di una sfera. Per ottenere o impostare il raggio, è possibile utilizzare la proprietà Raggio della classe Sphere. Di seguito è riportato il codice di esempio per impostare il raggio di una sfera.
---
{{% alert color="primary" %}} 

Questa funzione è supportata dalla versione 19.4 o maggiore.

{{% /alert %}} 
##  **Lavoro con il raggio della sfera**
Utilizzando Aspose.3D for .NET, puoi impostare il raggio di utilizzo di una sfera. Per ottenere o impostare il raggio, puoi utilizzare la proprietà `Radius` della classe `Sphere`. Di seguito è riportato il codice di esempio per impostare il raggio di una sfera.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Create a Scene
Scene scene = new Scene();
// Set Sphere Radius (Using Radius property you can get or set radius of Sphere)
scene.RootNode.CreateChildNode(new Sphere() { Radius = 10 });
// Save scene
scene.Save("sphere.obj");

{{< /highlight >}}
