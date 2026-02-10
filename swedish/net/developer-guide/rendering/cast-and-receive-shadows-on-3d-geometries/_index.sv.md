---
title: Kasta och ta emot skuggor på 3D Geometrier
type: docs
weight: 10
url: /sv/net/cast-and-receive-shadows-on-3d-geometries/
description: Generellt kan vissa 3D filformat lagra skuggrelaterade inställningar i geometri som FBX. Använder Aspose. 3D for .NET, kan utvecklare göra en bild genom att kartlägga skuggor från en ljuskällas synpunkt. Bildkvaliteten beror på ljuskällan, höjdvinkeln och avståndet mellan kameran och geometriska objekt.
---
{{% alert color="primary" %}}

Generellt kan vissa 3D filformat lagra skuggrelaterade inställningar i geometri som FBX. Med [Aspose.3D for .NET](https://products.aspose.com/3d/net/) kan utvecklare göra en bild genom att kartlägga skuggor från en ljuskällas synpunkt. Bildkvaliteten beror på ljuskällan, höjdvinkeln och avståndet mellan kameran och geometriska objekt.

{{% /alert %}}
##  **Kasta och ta emot skugga**
Som standard kastar alla objekt i scenen skuggor från en ljuskälla. Utvecklare kan också ta emot skuggor per objekt base i objektytan. Detta kodexempel avslöjar hur ljus- och kameraobjekt ska ställas in. Den skapar också ett plan och placerar tre objekt med olika färger och skugginställningar.

Alla geometrier har `CastShadows = true` och `ReceiveShadows=true`, skuggorna av röd ruta och torus kastade till planet, Den röda lådan tar inte emot skuggor och blå lådan kastar inte skuggor.
###  **Programmeringsprova**
Det här kodexemplet kastar och tar emot skuggor på 3D geometries.

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


**Redigeringsresultat**

![todo:image_alt_text](cast-and-receive-shadows-on-3d-geometries_1.png)
