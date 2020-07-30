---
title : "Render a scene into the cubemap with six faces" 
description : "" 
weight : 12060 
toc : false
type: docs
url: /net/developerguide/rendering/render+a+scene+into+the+cubemap+with+six+faces/
---

# Aspose.3D for .NET : Render a scene into the cubemap with six faces


Using [Aspose.3D for .NET API](https://www.aspose.com/products/3d/net), developers can render a scene into the cubemap with six faces and save all faces into the supported image formats.

## Capture a cubemap with six faces

In this article, we create a Camera and two Light objects to capture the cubemap, also create a cubemap render target with depth texture, create a viewport and finally get the cubemap texture. The ITextureCubemap class retrieves the cubemap texture and the CubeFaceData class allows to access faces of the cubemap, and then export into the supported image format.

### Programming Sample

This code example renders a scene into the cubemap with six faces and export into the image format.

**C#**

string path = @"D:\\Projects\\glTF-Sample-Models\\1.0\\VC\\glTF-Binary\\VC.glb";//load the sceneScene scene = new Scene(path);//create a camera for capturing the cube mapCamera cam = new Camera(ProjectionType.Perspective){    NearPlane = 0.1,    FarPlane = 200,    RotationMode = RotationMode.FixedDirection};scene.RootNode.CreateChildNode(cam).Transform.Translation = new Vector3(5, 6, 0);//create two lights to illuminate the scenescene.RootNode.CreateChildNode(new Light() {LightType = LightType.Point}).Transform.Translation = new Vector3(-10, 7, -10);scene.RootNode.CreateChildNode(new Light(){    Color = new Vector3(Color.CadetBlue)}).Transform.Translation = new Vector3(49, 0, 49); //create a rendererusing (var renderer = Renderer.CreateRenderer()){    //Create a cube map render target with depth texture, depth is required when rendering a scene.    IRenderTexture rt = renderer.RenderFactory.CreateCubeRenderTexture(new RenderParameters(false), 512, 512);    //a viewport is required on the render target    rt.CreateViewport(cam, RelativeRectangle.FromScale(0, 0, 1, 1));    renderer.Render(rt);    //now lets get the cubemap texture    ITextureCubemap cubemap = rt.Targets\[0\] as ITextureCubemap;    //we can directly save each face to disk by specifing the file name    CubeFaceData<string> fileNames = new CubeFaceData<string>()    {        Right = "right.png",        Left = "left.png",        Back = "back.png",        Front = "front.png",        Bottom = "bottom.png",        Top = "top.png"    };    //and call Save method    cubemap.Save(fileNames, ImageFormat.Png);    //or we just need to use the render result in memory, we can save it to CubeFaceData<Bitmap>    //CubeFaceData<Bitmap> bitmaps = new CubeFaceData<Bitmap>();    //cubemap.Save(bitmaps);    //bitmaps.Back.Save("back.bmp", ImageFormat.Bmp);}

