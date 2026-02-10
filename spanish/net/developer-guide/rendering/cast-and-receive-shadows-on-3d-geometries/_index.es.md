---
title: Reparto y recepción de sombras en geometrías 3D
type: docs
weight: 10
url: /es/net/cast-and-receive-shadows-on-3d-geometries/
description: En general, algunos formatos de archivo 3D pueden almacenar configuraciones relacionadas con la sombra en geometría como FBX. Usando Aspose.3D for .NET, los desarrolladores pueden renderizar una imagen mapeando sombras desde el punto de vista de una fuente de luz. La calidad de la imagen depende de la fuente de luz, el ángulo de elevación y la distancia entre la cámara y los objetos geométricos.
---
{{% alert color="primary" %}}

En general, algunos formatos de archivo 3D pueden almacenar configuraciones relacionadas con la sombra en geometría como FBX. Usando [Aspose.3D for .NET](https://products.aspose.com/3d/net/), los desarrolladores pueden renderizar una imagen mapeando sombras desde el punto de vista de una fuente de luz. La calidad de la imagen depende de la fuente de luz, el ángulo de elevación y la distancia entre la cámara y los objetos geométricos.

{{% /alert %}}
##  **Reparto y recepción de sombra**
Por defecto, todos los objetos de la escena proyectan sombras desde una fuente de luz. Los desarrolladores también pueden recibir sombras por objeto en la superficie del objeto. Este ejemplo de código revela cómo establecer la posición de la luz y los objetos de la cámara. También crea un plano y coloca tres objetos con diferentes colores y configuraciones de sombra.

Todas las geometrías tienen `CastShadows = true` y `ReceiveShadows=true`, las sombras de la caja roja y el toro se proyectan en el plano, la caja roja no recibirá sombras y la caja azul no proyectará sombras.
###  **Muestra de programación**
Este ejemplo de código proyecta y recibe sombras en geometrías 3D.

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


**Resultado de renderizado**

¡! [Todo: image_alt_text](cast-and-receive-shadows-on-3d-geometries_1.png)
