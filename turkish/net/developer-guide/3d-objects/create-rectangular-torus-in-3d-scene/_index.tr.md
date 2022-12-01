---
title: Create dikdörtgen Torus 3D cene cene
type: docs
weight: 50
url: /tr/net/create-rectangular-torus-in-3d-scene/
description: Using Aspose.3D for .NET API, geliştiriciler 3D nesnelerini oluşturabilir ve sonra 076. 481 formatındaki herhangi bir şekilde 076. 481 sahnesini kaydedebilir.
---
{{% alert color="primary" %}} 

Using[Aspose.3D for .NET](https://products.aspose.com/3d/net/)API, geliştiriciler 3D nesnelerini oluşturabilir ve 3D sahnesini desteklenen herhangi bir 3D formatında kaydedebilir.

{{% /alert %}} 
## **Angular ectangular Torus**
We `RectangularTorus` sınıfı ekledi, geliştiricilerin sahne içine parametreli dikdörtgen bir torus yerleştirmelerine izin veriyor, bu, sahneyi farklı desteklenen dosya formatlarına kaydederken sıra dışı örgü/üçgen örgüye dönüştürülebilir.

**C#**

{{< highlight "java" >}}

 RectangularTorus rt = new RectangularTorus();

rt.InnerRadius = 17;

rt.OuterRadius = 22;

rt.Height = 30;

rt.Arc = Math.PI * 0.5;

Scene scene = new Scene();

scene.RootNode.CreateChildNode(rt);

scene.Save("rtorus.obj", FileFormat.WavefrontOBJ);

{{< /highlight >}}

To dikdörtgen torus aşağıdaki gibi görünüyor:

![Todo: görüntü_Alt_Metin](create-rectangular-torus-in-3d-scene_1.png)
