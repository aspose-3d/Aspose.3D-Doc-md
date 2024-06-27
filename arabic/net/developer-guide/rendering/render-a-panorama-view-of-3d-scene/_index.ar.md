---
title: تقديم عرض بانورامي لمشهد 3D
type: docs
weight: 60
url: /ar/net/render-a-panorama-view-of-3d-scene/
description: باستخدام Aspose.3D for .NET API ، يمكن للمطورين عرض بانوراما لمشهد 3D وحفظ هذا العرض في تنسيقات الصور المدعومة.
---
{{% alert color="primary" %}}

باستخدام [Aspose.3D for .NET API](https://products.aspose.com/3d/net/) ، يمكن للمطورين عرض صورة بانورامية لمشهد 3D وحفظ هذا العرض في تنسيقات الصور المدعومة.

{{% /alert %}}
##  **Rereate عرض Panorama**
في هذه المقالة ، نقوم بإنشاء كاميرا وجسمان ضوئيان لالتقاط المشهد ، وكذلك إنشاء هدف عرض ، وإنشاء منفذ عرض وتنفيذ مرحلة ما بعد الإسقاط بشكل متساوي مستطيل مع خريطة مكعبة كمدخل وأخيراً حفظ نسيج بانوراما. تسمح طريقة `Execute` لفئة `Renderer` بتنفيذ تأثير معالجة النشر وحفظ النتيجة لتقديم الهدف.
###  **Pروغرامينغ ple وافرة**
هذا المثال الخاص بالرمز يعرض صورة بانورامية لمشهد 3D ويحفظ في تنسيق الصورة.

**C#**

{{< highlight "java" >}}

 string path = @"D:\Projects\glTF-Sample-Models\1.0\VC\glTF-Binary\VC.glb";

//load the scene

Scene scene = new Scene(path);

//create a camera for capturing the cube map

Camera cam = new Camera(ProjectionType.Perspective)

{

    NearPlane = 0.1,

    FarPlane = 200,

    RotationMode = RotationMode.FixedDirection

};

scene.RootNode.CreateChildNode(cam).Transform.Translation = new Vector3(5, 6, 0);



//create two lights to illuminate the scene

scene.RootNode.CreateChildNode(new Light() {LightType = LightType.Point}).Transform.Translation = new Vector3(-10, 7, -10);

scene.RootNode.CreateChildNode(new Light()

{

    Color = new Vector3(Color.CadetBlue)

}).Transform.Translation = new Vector3(49, 0, 49);

//create a renderer

using (var renderer = Renderer.CreateRenderer())

{

    //Create a cube map render target with depth texture, depth is required when rendering a scene.

    IRenderTexture rt = renderer.RenderFactory.CreateCubeRenderTexture(new RenderParameters(false), 512, 512);

    //create a 2D texture render target with no depth texture used for image processing

    IRenderTexture final = renderer.RenderFactory.CreateRenderTexture(new RenderParameters(false, 32, 0, 0), 1024 * 3 , 1024);



    //a viewport is required on the render target

    rt.CreateViewport(cam, RelativeRectangle.FromScale(0, 0, 1, 1));

    renderer.Render(rt);



    //execute the equirectangular projection post-processing with the previous rendered cube map as input

    PostProcessing equirectangular = renderer.GetPostProcessing("equirectangular");

    //Specify the cube map rendered from the scene as this post processing's input

    equirectangular.Input = rt.Targets[0];

    //Execute the post processing effect and save the result to render target final

    renderer.Execute(equirectangular, final);

    //save the texture into disk

    ((ITexture2D)final.Targets[0]).Save("panorama.png", ImageFormat.Png);

}

{{< /highlight >}}
