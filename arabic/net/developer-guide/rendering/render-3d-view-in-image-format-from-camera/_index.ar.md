---
title: تقديم عرض 3D بتنسيق صورة من الكاميرا
type: docs
weight: 50
url: /ar/net/render-3d-view-in-image-format-from-camera/
description: باستخدام Aspose.3D for .NET ، يمكن للمطورين عرض صورة لعرض صورة واقعية لطراز 3D ، مع أو بدون الخلفية المحسنة ، والقوام ، والظلال ، وكذلك ضبط حجم الصورة.
---
{{% alert color="primary" %}}

باستخدام [Aspose.3D for .NET](https://products.aspose.com/3d/net/) ، يمكن للمطورين عرض صورة لعرض صورة واقعية لطراز 3D ، مع أو بدون الخلفية المحسنة ، والقوام ، والظلال ، وكذلك ضبط حجم الصورة.

{{% /alert %}}
##  **التقط صورة لطراز 3D من الكاميرا**
يمكن استخدام طريقة `Render` التي تعرضها فئة [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) لالتقاط صورة من الكاميرا النشطة. يمكن للمطورين أيضًا استخدام عدة طرق مختلفة للتنقل ووضع الكاميرا في المشهد. في مثال الرمز هذا ، نقوم بإنشاء كاميرا في الموضع (10,10,10) في مشهد موجود 3D وننظر إلى نقطة الأصل للعرض.
###  **Pروغرامينغ ple وافرة**
يُنشئ مثال الرمز هذا كاميرا في مشهد 3D ، ويُحدد هدفها ويُعرض صورة.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET

                // Load scene from file
                Scene scene =  Scene.FromFile("camera.usdz");
                // Create a camera at (10,10,10) and look at the origin point for rendering,
                // It must be attached to the scene before render
                Camera camera = new Camera();
                scene.RootNode.CreateChildNode("camera", camera);
                camera.ParentNode.Transform.Translation = new Vector3(10, 10, 10);
                camera.LookAt = Vector3.Origin;

                // Specify the image render option
                ImageRenderOptions opt = new ImageRenderOptions();
                // Set the background color
                opt.BackgroundColor = Color.AliceBlue;
                // Tells renderer where the it can find textures
                opt.AssetDirectories.Add("textures");
                // Turn on shadow
                opt.EnableShadows = true;
                // Render the scene in given camera's perspective into specified png file with size 1024x1024
                scene.Render(camera, "Render3DModelImageFromCamera.png", new Size(1024, 1024), ImageFormat.Png, opt);

{{< /highlight >}}
