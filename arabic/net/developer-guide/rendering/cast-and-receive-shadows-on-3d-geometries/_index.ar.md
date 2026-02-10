---
title: يلقي الظلال ويتلقيها على أشكال أشكال حرف 3D
type: docs
weight: 10
url: /ar/net/cast-and-receive-shadows-on-3d-geometries/
description: بشكل عام ، يمكن لبعض تنسيقات الملفات 3D تخزين الإعدادات المتعلقة بالظل في الهندسة مثل FBX. باستخدام Aspose.3D for .NET ، يمكن للمطورين عرض صورة عن طريق تعيين الظلال من وجهة نظر مصدر الضوء. تعتمد جودة الصورة على مصدر الضوء وزاوية الارتفاع والمسافة بين الكاميرا والكائنات الهندسية.
---
{{% alert color="primary" %}}

بشكل عام ، يمكن لبعض تنسيقات الملفات 3D تخزين الإعدادات المتعلقة بالظل في الهندسة مثل FBX. باستخدام [Aspose.3D for .NET](https://products.aspose.com/3d/net/) ، يمكن للمطورين عرض صورة عن طريق تعيين الظلال من وجهة نظر مصدر الضوء. تعتمد جودة الصورة على مصدر الضوء وزاوية الارتفاع والمسافة بين الكاميرا والكائنات الهندسية.

{{% /alert %}}
##  **Cast و ecechadow hadow**
By الافتراضي ، كل الكائنات في المشهد يلقي الظلال من مصدر الضوء. قد تتلقى أيضا الظلال على أساس كل كائن في سطح الكائن. Tمثال له رمز يكشف كيفية تعيين موقف الأشياء الخفيفة والكاميرا. It أيضا يخلق طائرة ويضع ثلاثة كائنات بألوان مختلفة وإعدادات الظل.

تحتوي جميع الأشكال الجندرية على `CastShadows = true` و `ReceiveShadows=true` ، وظلال الصندوق الأحمر والنتوء المصبوب على الطائرة ، ولن يتلقى الصندوق الأحمر ظلالًا ولن يلقي الصندوق الأزرق ظلالًا.
###  **Pروغرامينغ ple وافرة**
هذا المثال البرمجي يلقي الظلال ويتلقى الظلال على 3D geumetries.

{{< highlight "csharp" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-.NET

                Scene scene = new Scene();
                Camera camera = new Camera();
                camera.NearPlane = 0.1;
                scene.RootNode.CreateChildNode("camera", camera);
                Light light;
                scene.RootNode.CreateChildNode("light", light = new Light()
                {
                    NearPlane = 0.1,
                    CastShadows = true,
                    Color = new Vector3(Color.White)
                }).Transform.Translation = new Vector3(9.4785, 5, 3.18);
                light.LookAt = Vector3.Origin;
                light.Falloff = 90;

                // Create a plane
                Node plane = scene.RootNode.CreateChildNode("plane", new Plane(20, 20));
                plane.Material = new PhongMaterial() { DiffuseColor = new Vector3(Color.DarkOrange) };
                plane.Transform.Translation = new Vector3(0, 0, 0);

                // Create a torus for casting shadows
                Mesh m = (new Torus("", 1, 0.4, 20, 20, Math.PI * 2)).ToMesh();
                Node torus = scene.RootNode.CreateChildNode("torus", m);
                torus.Material = new PhongMaterial() { DiffuseColor = new Vector3(Color.Cornsilk) };
                torus.Transform.Translation = new Vector3(2, 1, 1);

                { 
                    // Create a blue box don't cast shadows
                    m = (new Box()).ToMesh();
                    m.CastShadows = false;
                    Node box = scene.RootNode.CreateChildNode("box", m);
                    box.Material = new PhongMaterial() { DiffuseColor = new Vector3(Color.Blue) };
                    box.Transform.Translation = new Vector3(2, 1, -1);
                }
                {
                    // Create a red box that don't receive shadow but cast shadows
                    m = (new Box()).ToMesh();
                    m.ReceiveShadows = false;
                    Node box = scene.RootNode.CreateChildNode("box", m);
                    box.Material = new PhongMaterial() { DiffuseColor = new Vector3(Color.Red) };
                    box.Transform.Translation = new Vector3(-2, 1, 1);
                }
                camera.ParentNode.Transform.Translation = new Vector3(10, 10, 10);
                camera.LookAt = Vector3.Origin;
                ImageRenderOptions opt = new ImageRenderOptions() { EnableShadows = true };
                scene.Render(camera, "CastAndReceiveShadow_out.png", new Size(1024, 1024), ImageFormat.Png, opt);

{{< /highlight >}}


**Render R**

! [Todo: image_ altttext](cast-and-receive-shadows-on-3d-geometries_1.png)
