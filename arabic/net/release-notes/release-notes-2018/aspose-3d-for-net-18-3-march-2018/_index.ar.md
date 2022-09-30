---
title: Aspose.3D for .NET 18.3-قوس النصر 2018
type: docs
weight: 100
url: /ar/net/aspose-3d-for-net-18-3-march-2018/
---
{{% alert color="primary" %}} 

Tصفحته تحتوي على ملاحظات الإصدار ل[Aspose.3D for .NET 18.3](https://www.nuget.org/packages/Aspose.3D/18.3.0).

{{% /alert %}} 
## **Oأكثر ements المبروفات و hangمعلقة**

|**Key**|**Sأوماري**|**Category**|
|:- |:- |:- |
|THREEDNET-364|Order-الشفافية المستقلة|Enhancement|
|THREEDNET-359|3DS إلى GLTF تصدير يلقي من خطأ مؤشر|Bug|
|THREEDNET-358|Cannot تجعل شفافية النموذج|Bug|
### **Public API و ackأكواردز hangمتوافق مع hangمعلقة**
See قائمة أي تغييرات أجريت على الجمهور API مثل إضافة أو إعادة تسميتها أو إزالتها أو إهمال الأعضاء وكذلك أي تغيير متوافق غير متخلف تم إجراؤه على Aspose.3D for .NET. If لديك مخاوف حول أي تغيير المدرجة ، يرجى رفع على[Aspose.3D دعم المنتدى](https://forum.aspose.com/c/3d/18).
#### **طريقة ox dds إلى Aspose.ThreeD. Eفئة ntity**
**Defintion-C#**

{{< highlight "java" >}}

 /// <summary>

/// Gets the bounding box of current entity in its object space coordinate system.

/// </summary>

public Aspose.ThreeD.Utilities.BoundingBox GetBoundingBox()

{{< /highlight >}}

يمكن الحصول على صندوق الحدود للكيان في نظام تنسيق الجسم والفضاء الخاص به.

**Oقصيدة مثال-C#**

{{< highlight "java" >}}

 var box = new Box();

BoundingBox bbox = box.GetBoundingBox(); 

Console.WriteLine(bbox);

{{< /highlight >}}
#### **Adds enum نوع Aspose.ThreeD. hhading. lplphaSource**
**Defintion-C#**

{{< highlight "java" >}}

 /// <summary>

/// Defines whether the texture contains the alpha channel.

/// </summary>

public enum AlphaSource

{

    /// <summary>

    /// No alpha is defined in the texture

    /// </summary>

    None,

    /// <summary>

    /// The alpha is defined by pixel's alpha channel

    /// </summary>

    PixelAlpha,

    /// <summary>

    /// The Alpha is a fixed value which is defined by <see cref="TextureBase.Alpha"/> 

    /// </summary>

    FixedValue

}

{{< /highlight >}}
#### **أعضاء Adds Alpha و lplphaSource إلى Aspose.ThreeD.Shading. exextureBase الفئة**
**C#**

{{< highlight "java" >}}

 /// <summary>

/// Gets or sets the default alpha value of the texture

/// This is valid when the <see cref="AlphaSource"/> is <see cref="Aspose.ThreeD.Shading.AlphaSource.PixelAlpha"/>

/// Default value is 1.0, valid value range is between 0 and 1

/// </summary>

public double Alpha{ get;set;}

/// <summary>

/// Gets or sets whether the texture defines the alpha channel.

/// Default value is <see cref="Aspose.ThreeD.Shading.AlphaSource.None"/>

/// </summary>

public Aspose.ThreeD.Shading.AlphaSource AlphaSource{ get;set;}

{{< /highlight >}}

يتم إضافة أعضاء ese hese لجعلها متوافقة مع الملمس-الشفافية في الملفات 3D مثل U3D/FBX ، وهي مدعومة أيضا في المورد Aspose.3D. Since Aspose.ThreeD. hhading. amambertMaterial/Aspose.ThreeD. hhading. PhongMaterial/ Aspose.ThreeD. hhading.

**C#**

{{< highlight "java" >}}

 // define a box node with alpha channel defined in albedo texture:

var node = new Node()

{

    Material = new PbrMaterial()

    {

        AlbedoTexture = new Texture()

        {

            AlphaSource = AlphaSource.PixelAlpha,

            FileName = "window.tga"

        }

    },

    Entity = new Box()

};

{{< /highlight >}}
