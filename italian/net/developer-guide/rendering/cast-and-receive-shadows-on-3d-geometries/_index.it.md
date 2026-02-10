---
title: Lanciare e ricevere ombre su 3D geometrie
type: docs
weight: 10
url: /it/net/cast-and-receive-shadows-on-3d-geometries/
description: In generale, alcuni formati di file 3D possono memorizzare le impostazioni relative alle ombre in geometria come FBX. Utilizzando Aspose.3D for .NET, gli sviluppatori possono eseguire il rendering di un'immagine mappando le ombre dal punto di vista di una sorgente luminosa. La qualità dell'immagine dipende dalla sorgente luminosa, dall'angolo di elevazione e dalla distanza tra la fotocamera e gli oggetti geometrici.
---
{{% alert color="primary" %}}

In generale, alcuni formati di file 3D possono memorizzare le impostazioni relative alle ombre in geometria come FBX. Utilizzando [Aspose.3D for .NET](https://products.aspose.com/3d/net/), gli sviluppatori possono eseguire il rendering di un'immagine mappando le ombre dal punto di vista di una sorgente luminosa. La qualità dell'immagine dipende dalla sorgente luminosa, dall'angolo di elevazione e dalla distanza tra la fotocamera e gli oggetti geometrici.

{{% /alert %}}
##  **Trasmetti e ricevi l'ombra**
Per impostazione predefinita, tutti gli oggetti nella scena proiettano ombre da una sorgente luminosa. Gli sviluppatori possono anche ricevere ombre su base per oggetto nella superficie dell'oggetto. Questo esempio di codice rivela come impostare la posizione della luce e degli oggetti della fotocamera. Crea anche un piano e posiziona tre oggetti con diversi colori e impostazioni dell'ombra.

Tutte le geometrie hanno `CastShadows = true` e `ReceiveShadows=true`, le ombre della scatola rossa e del toro gettate sull'aereo, la scatola rossa non riceverà ombre e la scatola blu non proietterà ombre.
###  **Campione di programmazione**
Questo esempio di codice proietta e riceve ombre su geometrie 3D.

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


**Risultato di rendering**

! [Todo: image_alt_text](cast-and-receive-shadows-on-3d-geometries_1.png)
