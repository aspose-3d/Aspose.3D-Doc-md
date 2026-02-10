---
title: Arbeta med sfärens radie
type: docs
weight: 110
url: /sv/net/working-with-radius-of-sphere/
description: Genom att använda Aspose.3D for .NET kan du hämta radie av en sfär. För att få eller ställa in radien, kan du använda Radius egenskap av sfärklassen. Nedan följer kodprovet för att ställa in en sfärs radie.
---
{{% alert color="primary" %}} 

Denna funktion stöds av version 19.4 eller större.

{{% /alert %}} 
##  **Arbeta med sfärens radie**
Genom att använda Aspose.3D for .NET kan du hämta radie av en sfär. För att få eller ställa in radie kan du använda `Radius`-egenskapen i klassen `Sphere`. Nedan följer kodprovet för att ställa in en sfärs radie.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Create a Scene
Scene scene = new Scene();
// Set Sphere Radius (Using Radius property you can get or set radius of Sphere)
scene.RootNode.CreateChildNode(new Sphere() { Radius = 10 });
// Save scene
scene.Save("sphere.obj");

{{< /highlight >}}
