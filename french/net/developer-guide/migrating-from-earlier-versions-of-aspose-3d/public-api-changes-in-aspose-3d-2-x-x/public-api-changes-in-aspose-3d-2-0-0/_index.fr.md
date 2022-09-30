---
title: Public API Changements dans Aspose.3D 2.0.0
type: docs
weight: 20
url: /fr/net/public-api-changes-in-aspose-3d-2-0-0/
---
**Résumé du contenu**

- [Ajoute le format Collada](#PublicAPIChangesinAspose.3D2.0.0-AddsColladaformat)
- [Ajoute Aspose.ThreeD. Rendre. Interfaces IRenderTarget/IRenderTexture/IRenderWindow/ItextureUnit et Aspose.ThreeD.Render.Viewport/InitialisationException/RendererType/TextureType/DriverException/RenderFactory/RenderParamètres classes](#PublicAPIChangesinAspose.3D2.0.0-AddsAspose.ThreeD.Render.IRenderTarget/IRenderTexture/IRenderWindow/ITextureUnitinterfacesandAspose.ThreeD.Render.Viewport/InitializationException/Renderer/TextureType/DriverException/RenderFactory/RenderParametersclasses)
- [Ajoute Aspose.ThreeD. Rendre. Classe de post-traitement](#PublicAPIChangesinAspose.3D2.0.0-AddsAspose.ThreeD.Render.PostProcessingclass)
- [Ajoute la méthode GetBoundingBox à Aspose.ThreeD. Classe de nœud, ajoute les nouvelles classes Aspose.ThreeD. Utilitaires. BoundingBox et Aspose.ThreeD. Utilitaires. BoundingBoxExtent](#PublicAPIChangesinAspose.3D2.0.0-AddsGetBoundingBoxmethodtoAspose.ThreeD.Nodeclass,AddsnewclassesAspose.ThreeD.Utilities.BoundingBoxandAspose.ThreeD.Utilities.BoundingBoxExtent)
- [Rendu en temps réel](#PublicAPIChangesinAspose.3D2.0.0-Real-timeRendering)
- [Les méthodes AddData sont ajoutées au Aspose.ThreeD. Entités. Classe VertexElementUV](#PublicAPIChangesinAspose.3D2.0.0-AddDatamethodsareaddedtoAspose.ThreeD.Entities.VertexElementUVclass)

{{% alert color="primary" %}} 

Ce document décrit les modifications apportées au Aspose.3D API de la version 1.7.0 à 2.0.0, qui peuvent intéresser les développeurs de modules/applications. Il comprend non seulement des méthodes publiques nouvelles et mises à jour, mais également une description de tout changement de comportement dans les coulisses du Aspose.3D.

{{% /alert %}} 
### **Ajoute le format Collada**
Dans cette version (2.0.0), les développeurs peuvent importer des fichiers Collada 3D, de sorte que la propriété Collada est ajoutée dans la classe Aspose.ThreeD.FileFormat.
### **Ajoute Aspose.ThreeD. Rendre. Interfaces IRenderTarget/IRenderTexture/IRenderWindow/ItextureUnit et Aspose.ThreeD.Render.Viewport/InitialisationException/RendererType/TextureType/DriverException/RenderFactory/RenderParamètres classes**
Les nouvelles classes Viewport et Renderer sont les classes principales qui aident à capturer les vues d'une scène 3D et à les enregistrer dans une texture ou une fenêtre. Tous les détails des autres classes d'aide sont les suivants:

- **Aspose.ThreeD. Rendre. Classe DriverException**-Les exceptions du moteur de rendu interne sont emballées comme DriverException.
- **Aspose.ThreeD. Rendre. InitialisationClasse d'exception**-Cette exception est levée sans initialiser le moteur de rendu, par exemple pour l'initialiser sur un ordinateur qui n'a pas de support matériel de OpenGL 4.0.
- **Interface IRenderTarget**-C'est l'interface de base d'IRenderTexture/IRenderWindow.
- **Interface IRenderTexture**-Il permet de rendre la scène à une ou plusieurs textures (les textures sont situées dans la mémoire vidéo et peuvent être transférées à la mémoire système).
- **Interface de fenêtre IRender**-Il permet de rendre la scène à la fenêtre en temps réel.
- **ItextureUnit interface**-ItextureUnit est l'échantillonneur de texture du côté GPU et les données de texture dans la mémoire CPU ou GPU.
- **TextureType enum**-Il définit le type de textures, comme Texture1D, Texture2D, Texture3D, CubeMap et Array2D.
- **Classe RenderFactory**-Il aide à rendre une scène à des textures ou une fenêtre en temps réel.
- **Classe de RenderParamètres**-Il définit les paramètres sur la façon de créer la cible de rendu comme les bits de couleur, les bits de profondeur, les bits de pochoir et la double mémoire tampon.

**Capturez les Viewports d'une scène 3D et la rendre à une texture ou une fenêtre**

**C#**

{{< highlight "csharp" >}}

 // load an existing 3D scene

Scene scene = new Scene("scene.obj");

// create an instance of the camera

Camera camera = new Camera();

scene.RootNode.CreateChildNode("camera", camera).Transform.Translation = new Vector3(2, 44, 66);

// set the target

camera.LookAt = new Vector3(50, 12, 0);

//create a light

scene.RootNode.CreateChildNode("light", new Light() {Color = new Vector3(Color.White), LightType =  LightType.Point}).Transform.Translation = new Vector3(26, 57, 43);

// the CreateRenderer will create a hardware OpenGL-backend renderer

// and some internal initializations will be done.

// when the renderer left using the scope, the unmanaged hardware resources will also be disposed

using (var renderer = Renderer.CreateRenderer())

{

    renderer.EnableShadows = false;

    // create a new render target that renders the scene to texture(s)

    // use default render parameters

    // and one output targets

    // size is 1024 x 1024

    // this render target can have multiple render output textures, but here we only need one output.

    // The other textures and depth textures are mainly used by deferred shading in the future.

    // but you can also access the depth texture through IRenderTexture.DepthTeture

    // use CreateRenderWindow method to render in window, like:

    // window = renderer.RenderFactory.CreateRenderWindow(new RenderParameters(), Handle);

    using (IRenderTexture rt = renderer.RenderFactory.CreateRenderTexture(new RenderParameters(), 1, 1024, 1024))

    {

        //this render target has one viewport to render, the viewport occupies the 100% width and 100% height

        Viewport vp = rt.CreateViewport(camera, new RelativeRectangle() {ScaleWidth = 1, ScaleHeight = 1});

        //render the target and save the target texture to external file

        renderer.Render(rt);

        rt.Targets[0].Save("file-1viewports.png", ImageFormat.Png);

        //now let's change the previous viewport only uses the half left side(50% width and 100% height)

        vp.Area = new RelativeRectangle() {ScaleWidth = 0.5f, ScaleHeight = 1};

        //and create a new viewport that occupies the 50% width and 100% height and starts from 50%

        //both of them are using the same camera, so the rendered content should be the same

        rt.CreateViewport(camera, new RelativeRectangle() {ScaleX = 0.5f, ScaleWidth = 0.5f, ScaleHeight = 1});

        //but this time let's increase the field of view of the camera to 90 degree so it can see more part of the scene

        camera.FieldOfView = 90;

        renderer.Render(rt);

        rt.Targets[0].Save("file-2viewports.png", ImageFormat.Png);

    }

}

{{< /highlight >}}
### **Ajoute Aspose.ThreeD. Rendre. Classe de post-traitement**
La classe PostProcessing permet aux développeurs d'appliquer un filtre de traitement d'image en temps réel à l'image rendue. Dans cette version 2.0.0, nous avons fourni 4 effets de post-traitement intégrés. Nous autoriserons les développeurs à avoir leur propre algorithme de post-traitement personnalisé dans la future version.

**Appliquer des effets visuels pour économiser 3D vues**

**C#**

{{< highlight "csharp" >}}

 // load an existing 3D scene

Scene scene = new Scene("scene.obj");

// create an instance of the camera

Camera camera = new Camera();

scene.RootNode.CreateChildNode("camera", camera).Transform.Translation = new Vector3(2, 44, 66);

// set the target

camera.LookAt = new Vector3(50, 12, 0);

//create a light

scene.RootNode.CreateChildNode("light", new Light() { Color = new Vector3(Color.White), LightType = LightType.Point }).Transform.Translation = new Vector3(26, 57, 43);

// the CreateRenderer will create a hardware OpenGL-backend renderer, more renderer will be added in the future

// and some internal initializations will be done.

// when the renderer left using the scope, the unmanaged hardware resources will also be disposed

using (var renderer = Renderer.CreateRenderer())

{

    renderer.EnableShadows = false;

    // create a new render target that renders the scene to texture(s)

    // use default render parameters

    // and one output targets

    // size is 1024 x 1024

    // this render target can have multiple render output textures, but here we only need one output.

    // The other textures and depth textures are mainly used by deferred shading in the future.

    // but you can also access the depth texture through IRenderTexture.DepthTeture

    using (IRenderTexture rt = renderer.RenderFactory.CreateRenderTexture(new RenderParameters(), 1, 1024, 1024))

    {

        // this render target has one viewport to render, the viewport occupies the 100% width and 100% height

        Viewport vp = rt.CreateViewport(camera, new RelativeRectangle() { ScaleWidth = 1, ScaleHeight = 1 });

        //render the target and save the target texture to external file

        renderer.Render(rt);

        rt.Targets[0].Save("Original_viewport.png", ImageFormat.Png);

        // create a post-processing effect

        PostProcessing pixelation = renderer.GetPostProcessing("pixelation");

        renderer.PostProcessings.Add(pixelation);

        renderer.Render(rt);

        rt.Targets[0].Save("VisualEffect_pixelation.png", ImageFormat.Png);

        //clear previous post-processing effects and try another one

        PostProcessing grayscale = renderer.GetPostProcessing("grayscale");

        renderer.PostProcessings.Clear();

        renderer.PostProcessings.Add(grayscale);

        renderer.Render(rt);

        rt.Targets[0].Save("VisualEffect_grayscale.png", ImageFormat.Png);

        //we can also combine post-processing effects

        renderer.PostProcessings.Clear();

        renderer.PostProcessings.Add(grayscale);

        renderer.PostProcessings.Add(pixelation);

        renderer.Render(rt);

        rt.Targets[0].Save("VisualEffect_grayscale+pixelation.png", ImageFormat.Png);

        //clear previous post-processing effects and try another one

        PostProcessing edgedetection = renderer.GetPostProcessing("edge-detection");

        renderer.PostProcessings.Clear();

        renderer.PostProcessings.Add(edgedetection);

        renderer.Render(rt);

        rt.Targets[0].Save("VisualEffect_edgedetection.png", ImageFormat.Png);

        //clear previous post-processing effects and try another one

        PostProcessing blur = renderer.GetPostProcessing("blur");

        renderer.PostProcessings.Clear();

        renderer.PostProcessings.Add(blur);

        renderer.Render(rt);

        rt.Targets[0].Save("VisualEffect_blur.png", ImageFormat.Png);

    }

}

{{< /highlight >}}
### **Ajoute la méthode GetBoundingBox à Aspose.ThreeD. Classe de nœud, ajoute les nouvelles classes Aspose.ThreeD. Utilitaires. BoundingBox et Aspose.ThreeD. Utilitaires. BoundingBoxExtent**
Les classes BoundingBox et BoundingBoxExtent représentent la boîte enroulante d'un nœud 3D. Les développeurs peuvent réinitialiser l'appareil photo et calculer l'élévation à partir de la boîte enroulante. La boîte enroulante infinie ou nulle signifie que la scène n'a pas de géométries et n'ajuste l'élévation de la caméra que lorsqu'elle est finie.
### **Rendu en temps réel**
Il permet aux développeurs d'effectuer un rendu en temps réel haute performance sur un framework GUI comme WinForms, il est indépendant du cadre GUI, donc les autres frameworks GUI devraient également prendre en charge cela.
### **Les méthodes AddData sont ajoutées au Aspose.ThreeD. Entités. Classe VertexElementUV**
La classe de base du VertexElementUV a changé de VertexElementTemplate<Vector2>À VertexElementTemplate<Vector4>, Il ne stockera Vector4 que depuis 2.0.0, donc deux méthodes d'assistance ont été ajoutées pour permettre à l'utilisateur d'ajouter une liste de Vector2 et Vector3 à VertexElementUV, il étendra en interne Vector2/Vector3 à Vector4 et laissera les champs de repos zéro:
