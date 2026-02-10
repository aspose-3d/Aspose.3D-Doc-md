---
title: Werfen und empfangen Sie Schatten auf 3D Geometrien
type: docs
weight: 10
url: /de/net/cast-and-receive-shadows-on-3d-geometries/
description: Im Allgemeinen können einige 3D-Dateiformate schatten bezogene Einstellungen in Geometrie wie FBX speichern. Mit Aspose.3D for .NET können Entwickler ein Bild rendern, indem sie Schatten aus der Sicht einer Lichtquelle zuordnen. Die Bildqualität hängt von der Lichtquelle, dem Höhenwinkel und dem Abstand zwischen der Kamera und den geometrischen Objekten ab.
---
{{% alert color="primary" %}}

Im Allgemeinen können einige 3D-Dateiformate schatten bezogene Einstellungen in Geometrie wie FBX speichern. Mit [Aspose.3D for .NET](https://products.aspose.com/3d/net/) können Entwickler ein Bild rendern, indem sie Schatten aus der Sicht einer Lichtquelle zuordnen. Die Bildqualität hängt von der Lichtquelle, dem Höhenwinkel und dem Abstand zwischen der Kamera und den geometrischen Objekten ab.

{{% /alert %}}
##  **Schatten werfen und empfangen**
Standard mäßig werfen alle Objekte in der Szene Schatten von einer Lichtquelle. Entwickler können auch Schatten pro Objekt basis in der Objekt oberfläche erhalten. Dieses Code beispiel zeigt, wie die Position von Licht-und Kamera objekten eingestellt wird. Es erstellt auch eine Ebene und platziert drei Objekte mit unterschied lichen Farben und Schatten einstellungen.

Alle Geometrien haben `CastShadows = true` und `ReceiveShadows=true`, die Schatten von Red Box und Torus werden in das Flugzeug geworfen, die rote Box erhält keine Schatten und die blaue Box wirft keine Schatten.
###  **Programmier probe**
Dieses Code beispiel wirft und empfängt Schatten auf 3D Geometrien.

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


**Rendern Ergebnis**

! [Todo: image_alt_text](cast-and-receive-shadows-on-3d-geometries_1.png)
