---
title: Lancer et recevoir des ombres sur les géométries 3D
type: docs
weight: 10
url: /fr/net/cast-and-receive-shadows-on-3d-geometries/
description: Généralement, certains formats de fichiers 3D peuvent stocker des paramètres liés à l'ombre dans la géométrie comme FBX. En utilisant Aspose.3D for .NET, les développeurs peuvent rendre une image en cartographiant les ombres du point de vue d'une source lumineuse. La qualité d'image dépend de la source lumineuse, de l'angle d'élévation et de la distance entre la caméra et les objets géométriques.
---
{{% alert color="primary" %}}

Généralement, certains formats de fichiers 3D peuvent stocker des paramètres liés à l'ombre dans la géométrie comme FBX. En utilisant [Aspose.3D for .NET](https://products.aspose.com/3d/net/), les développeurs peuvent rendre une image en cartographiant les ombres du point de vue d'une source de lumière. La qualité d'image dépend de la source lumineuse, de l'angle d'élévation et de la distance entre la caméra et les objets géométriques.

{{% /alert %}}
##  **Cast et recevoir de l'ombre**
Par défaut, tous les objets de la scène projettent des ombres à partir d'une source lumineuse. Les développeurs peuvent également recevoir des ombres par objet dans la surface de l'objet. Cet exemple de code révèle comment définir la position de la lumière et des objets de l'appareil photo. Il crée également un plan et place trois objets avec des couleurs et des paramètres d'ombre différents.

Toutes les géométries ont `CastShadows = true` et `ReceiveShadows=true`, les ombres de la boîte rouge et du tore coulées sur le plan, la boîte rouge ne recevra pas d'ombres et la boîte bleue ne jettera pas d'ombres.
###  **Échantillon de programmation**
Cet exemple de code jette et reçoit des ombres sur les géométries 3D.

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


**Render Résultat**

! [Tout le monde: image_alt_text](cast-and-receive-shadows-on-3d-geometries_1.png)
