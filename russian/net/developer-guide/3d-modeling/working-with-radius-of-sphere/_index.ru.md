---
title: Работа с радиусом сферы
type: docs
weight: 110
url: /ru/net/working-with-radius-of-sphere/
description: Используя Aspose.3D for .NET, можно задать радиус получения сферы. Для того чтобы получить или задать радиус, вы можете использовать свойство Radius класса Sphere. Ниже приведен пример кода для установки радиуса сферы.
---
{{% alert color="primary" %}} 

Эта функция поддерживается версией 19,4 или выше.

{{% /alert %}} 
##  **Работа с радиусом сферы**
Используя Aspose.3D for .NET, можно задать радиус получения сферы. Чтобы получить или задать радиус, вы можете использовать свойство `Radius` класса `Sphere`. Ниже приведен пример кода для установки радиуса сферы.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Create a Scene
Scene scene = new Scene();
// Set Sphere Radius (Using Radius property you can get or set radius of Sphere)
scene.RootNode.CreateChildNode(new Sphere() { Radius = 10 });
// Save scene
scene.Save("sphere.obj");

{{< /highlight >}}
