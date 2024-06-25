---
title: Público API Cambios en Aspose.3D 2.0.0
type: docs
weight: 20
url: /es/net/public-api-changes-in-aspose-3d-2-0-0/
---
**Resumen de contenidos**

- [Agrega el formato Collada](#PublicAPIChangesinAspose.3D2.0.0-AddsColladaformat)
- [Agrega interfaces Aspose.ThreeD.Render.IRenderTarget/IRenderTexture/IRenderWindow/ITextureUnit y Aspose.ThreeD.Render.Viewport/InitializationException/Renderer/TextureType/DriverException/RenderFactory/Renderclasses ParameParameters](#PublicAPIChangesinAspose.3D2.0.0-AddsAspose.ThreeD.Render.IRenderTarget/IRenderTexture/IRenderWindow/ITextureUnitinterfacesandAspose.ThreeD.Render.Viewport/InitializationException/Renderer/TextureType/DriverException/RenderFactory/RenderParametersclasses)
- [Agrega la clase Aspose.ThreeD.Render.PostProcessing](#PublicAPIChangesinAspose.3D2.0.0-AddsAspose.ThreeD.Render.PostProcessingclass)
- [Agrega el método GetBoundingBox a la clase Aspose.ThreeD.Node, Agrega clases nuevas Aspose.ThreeD.Utilities.BoundingBox y Aspose.ThreeD.Utilities.BoundingBoxExtent](#PublicAPIChangesinAspose.3D2.0.0-AddsGetBoundingBoxmethodtoAspose.ThreeD.Nodeclass,AddsnewclassesAspose.ThreeD.Utilities.BoundingBoxandAspose.ThreeD.Utilities.BoundingBoxExtent)
- [Reproducción en tiempo real](#PublicAPIChangesinAspose.3D2.0.0-Real-timeRendering)
- [Los métodos AddData se agregan a la clase Aspose.ThreeD.Entities.VertexElementUV](#PublicAPIChangesinAspose.3D2.0.0-AddDatamethodsareaddedtoAspose.ThreeD.Entities.VertexElementUVclass)

{{% alert color="primary" %}} 

This document describes changes to the Aspose.3D API from version 1.7.0 to 2.0.0, that may be of interest to module/application developers. It includes not only new and updated public methods, but also a description of any changes in the behavior behind the scenes in Aspose.3D.

{{% /alert %}} 
###  **Agrega el formato Collada**
En esta versión (2.0.0), los desarrolladores pueden importar archivos Collada 3D, por lo que la propiedad Collada se agrega en la clase Aspose.ThreeD.FileFormat.
###  **Agrega interfaces Aspose.ThreeD.Render.IRenderTarget/IRenderTexture/IRenderWindow/ITextureUnit y Aspose.ThreeD.Render.Viewport/InitializationException/Renderer/TextureType/DriverException/RenderFactory/Renderclasses ParameParameters**
Las nuevas clases Viewport y Renderer son las clases principales que ayudan a capturar las vistas de una escena 3D y guardar en una textura o ventana. Todos los detalles de otras clases de ayuda son los siguientes:

- **Aspose.ThreeD.Render.DriverException (clase)**-Las excepciones del renderizador interno se envuelven como DriverException.
- **Aspose.ThreeD.Render.InitializationException (clase)**-Esta excepción se lanza mientras no se inicializa el renderizador, por ejemplo, para inicializarlo en un equipo que no tiene soporte de hardware OpenGL 4,0.
- **Interfaz IRenderTarget**-Es la interfaz base de IRenderTexture/IRenderWindow.
- **IRenderTexture interfaz**-Permite renderizar la escena a una o más texturas (las texturas se encuentran en la memoria de vídeo y se pueden transferir a la memoria del sistema).
- **Interfaz IRenderWindow**-Permite renderizar la escena a la ventana en tiempo real.
- **Interfaz ITextureUnit**-ITextureUnit es el muestreador de textura en el lado de la GPU y los datos de textura en la memoria de la CPU o GPU.
- **TextureType enum**-Define el tipo de texturas, como Texture1D, Texture2D, Texture3D, CubeMap y Array2D.
- **Clase RenderFactory**-Ayuda a renderizar una escena a texturas o ventanas en tiempo real.
- **RenderParameters clase**-Define los parámetros sobre cómo crear el objetivo de render como bits de color, bits de profundidad, bits de plantilla y doble búfer.

**Capturar los Viewports de una escena 3D y render a una textura o ventana**

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
###  **Agrega la clase Aspose.ThreeD.Render.PostProcessing**
La clase PostProcessing permite a los desarrolladores aplicar un filtro de procesamiento de imágenes en tiempo real a la imagen renderizada. En esta versión 2.0.0, hemos proporcionado 4 efectos de post-procesamiento incorporados. Permitiremos a los desarrolladores tener su propio algoritmo de posprocesamiento personalizado en la versión futura.

**Aplicar efectos visuales al guardar las vistas 3D**

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
###  **Agrega el método GetBoundingBox a la clase Aspose.ThreeD.Node, Agrega clases nuevas Aspose.ThreeD.Utilities.BoundingBox y Aspose.ThreeD.Utilities.BoundingBoxExtent**
Las clases BoundingBox y BoundingBoxExtent representan el cuadro delimitador de un nodo 3D. Los desarrolladores pueden restablecer la cámara y calcular la elevación desde el cuadro delimitador. El cuadro delimitador infinito o nulo significa que la escena no tiene geometrías y solo ajusta la elevación de la cámara cuando es finita.
###  **Reproducción en tiempo real**
Permite a los desarrolladores realizar renderizado en tiempo real de alto rendimiento en un marco GUI como WinForms, es independiente del marco GUI, por lo que los otros marcos GUI también deberían admitir esto.
###  **Los métodos AddData se agregan a la clase Aspose.ThreeD.Entities.VertexElementUV**
La clase base de VertexElementUV ha cambiado de VertexElementTemplate<Vector2>A VertexelementTemplate<Vector4>, Solo almacenará Vector4 desde 2.0.0, por lo que se agregaron dos métodos de ayuda para permitir al usuario agregar una lista de Vector2 y Vector3 a VertexElementUV, expandirá internamente el Vector2/Vector3 a Vector4 y dejará el resto campos cero:
