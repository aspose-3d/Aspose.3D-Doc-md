---
title: Бросайте и получайте тени на геометрии 3D
type: docs
weight: 10
url: /ru/net/cast-and-receive-shadows-on-3d-geometries/
description: Как правило, некоторые форматы файлов 3D могут хранить настройки, связанные с тенью, в геометрии, например FBX. Используя Aspose.3D for .NET, разработчики могут визуализировать изображение, отображая тени с точки зрения источника света. Качество изображения зависит от источника света, угла возвышения и расстояния между камерой и геометрическими объектами.
---
{{% alert color="primary" %}}

Как правило, некоторые форматы файлов 3D могут хранить настройки, связанные с тенью, в геометрии, например FBX. Используя [Aspose.3D for .NET](https://products.aspose.com/3d/net/), разработчики могут визуализировать изображение, отображая тени с точки зрения источника света. Качество изображения зависит от источника света, угла возвышения и расстояния между камерой и геометрическими объектами.

{{% /alert %}}
##  **В ролях и получайте тень**
По умолчанию все объекты в сцене отбрасывают тени от источника света. Разработчики также могут получать тени на основе каждого объекта на поверхности объекта. Этот пример кода показывает, как установить положение света и объектов камеры. Он также создает плоскость и размещает три объекта с разными цветами и настройками теней.

Все геометрии имеют `CastShadows = true` и `ReceiveShadows=true`, тени красного ящика и тора, наложенные на плоскость, красный ящик не будет получать тени, а синий блок не будет отбрасывать тени.
###  **Образец программирования**
Этот пример кода отбрасывает и получает тени на геометрии 3D.

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


**Результат Render**

! [Для: имаге_альт_текст](cast-and-receive-shadows-on-3d-geometries_1.png)
