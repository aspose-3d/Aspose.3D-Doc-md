---
title: Working مع Radius من Sphere
type: docs
weight: 110
url: /ar/net/working-with-radius-of-sphere/
description: باستخدام Aspose.3D for .NET ، يمكنك ضبط الحصول على نصف قطر كروي. من أجل الحصول على أو ضبط نصف القطر ، يمكنك استخدام خاصية نصف القطر لفئة كروية. فيما يلي عينة الكود لتعيين نصف قطر كروي.
---
{{% alert color="primary" %}} 

Tويدعم ميزة له من قبل الإصدار 19.4 أو أكبر.

{{% /alert %}} 
##  **Work مع Radius من Sphere**
باستخدام Aspose.3D for .NET ، يمكنك ضبط الحصول على نصف قطر كروي. من أجل الحصول على نصف قطر أو ضياعه ، يمكنك استخدام خاصية `Radius` من فئة `Sphere`. فيما يلي عينة الكود لتعيين نصف قطر كروي.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET
// Create a Scene
Scene scene = new Scene();
// Set Sphere Radius (Using Radius property you can get or set radius of Sphere)
scene.RootNode.CreateChildNode(new Sphere() { Radius = 10 });
// Save scene
scene.Save("sphere.obj");

{{< /highlight >}}
