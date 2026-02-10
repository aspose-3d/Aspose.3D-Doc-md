---
title: Cast and Receive Shadows on 3D Geometries
type: docs
weight: 10
url: /tr/net/cast-and-receive-shadows-on-3d-geometries/
description: Generally, some 3D file formats can store shadow related settings in geometry like FBX. Using Aspose.3D for .NET, developers can render an image by mapping shadows from the viewpoint of a light source. The image quality depends on the light source, elevation angle and distance between the camera and geometric objects.
---
{{% alert color="primary" %}}

Generally, some 3D file formats can store shadow related settings in geometry like FBX. Using [Aspose.3D for .NET](https://products.aspose.com/3d/net/), developers can render an image by mapping shadows from the viewpoint of a light source. The image quality depends on the light source, elevation angle and distance between the camera and geometric objects.

{{% /alert %}}
##  **Cast ve Reeve Shadow**
Varsayılan olarak, sahnedeki tüm nesneler bir ışık kaynağından gölgeler döküyor. Developers, nesne yüzeyinde nesne bazında da gölgeler alabilir. Tkod örneği, ışık ve kamera nesnelerinin konumunu nasıl ayarlayacağını gösterir. It ayrıca bir uçak oluşturur ve farklı renkler ve gölge ayarları ile üç nesne yerleştirir.

All geometries has `CastShadows = true` and `ReceiveShadows=true`, the shadows of red box and torus casted to the plane, the red box won't receive shadows and blue box won't cast shadows.
###  **Programming ample ample**
This code example casts and Receives shadows on 3D geometries.

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


**Render esuesult**

! [Todo: image_alt_text](cast-and-receive-shadows-on-3d-geometries_1.png)
