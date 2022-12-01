---
title: Aspose.3D for .NET 18,3 - mars 2018
type: docs
weight: 100
url: /sv/net/aspose-3d-for-net-18-3-march-2018/
---
{{% alert color="primary" %}} 

Denna sida innehåller utgåvans anteckningar för[Aspose.3D for .NET 18,3](https://www.nuget.org/packages/Aspose.3D/18.3.0).

{{% /alert %}} 
## **Andra förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|THREEDNET-364|Beställningsberoende öppenhet|Förbättring|
|THREEDNET-359|3DS till GLTF exporten kastar utanför indexfelel|FelComment|
|THREEDNET-358|Kan inte göra modellen genomskinlighet|FelComment|
### **Offentlig API och bakåts oförenliga förändringar**
Se förteckningen över eventuella ändringar i allmänheten API såsom lagts till, bytt namn, Avlägsnade eller förlåtna medlemmar samt eventuella icke-tillbaka-kompatibla förändringar till Aspose.3D for .NET. Om du har farhågor om någon förändring som anges, vänligen ta upp det om[Aspose.3D stödforum](https://forum.aspose.com/c/3d/18).
#### **Lägger till GetBoundingBox metod till Aspose.ThreeD.Entity klass**
**Definition - C#**

{{< highlight "java" >}}

 /// <summary>

/// Gets the bounding box of current entity in its object space coordinate system.

/// </summary>

public Aspose.ThreeD.Utilities.BoundingBox GetBoundingBox()

{{< /highlight >}}

Utvecklare kan få enhetens avgränsande ruta i sitt eget objekt-rymd koordinatsystem.

**Kodexempel - C#**

{{< highlight "java" >}}

 var box = new Box();

BoundingBox bbox = box.GetBoundingBox(); 

Console.WriteLine(bbox);

{{< /highlight >}}
#### **Lägger till enumtyp Aspose.ThreeD.Shading.Källa**
**Definition - C#**

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
#### **Lägger till alfa- och AlphaSource-medlemmar till Aspose.ThreeD.Shading.TextureBase klass**
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

Dessa medlemmar läggs till för att göra det kompatibel med textur transparens i 3D filer som U3D/07611 23481, Dessa stöds också i Aspose.3D renderare. Sedan Aspose.ThreeD. Skuggande. LambertMaterial/ Aspose.ThreeD. Skuggande. PhongMaterial/ Aspose.ThreeD. Skuggande. PbrMaterial har en TransparencyFactor, men det är inte långt tillräckligt för vissa komplexa transparensmaterial, efter 18.3, material kan använda per-pixel alfakanal som definieras i diffusa/albedo-strukturen.

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
