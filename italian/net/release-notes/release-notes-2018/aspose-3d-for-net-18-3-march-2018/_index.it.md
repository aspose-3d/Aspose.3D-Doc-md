---
title: Aspose.3D for .NET 18.3-marzo 2018
type: docs
weight: 100
url: /it/net/aspose-3d-for-net-18-3-march-2018/
---
{{% alert color="primary" %}} 

Questa pagina contiene le note di rilascio per[Aspose.3D for .NET 18.3](https://www.nuget.org/packages/Aspose.3D/18.3.0).

{{% /alert %}} 
## **Altri miglioramenti e modifiche**

|**Chiave**|**Riassunto**|**Categoria**|
|:- |:- |:- |
|THREEDNET-364|Trasparenza indipendente dall'ordine|Miglioramento|
|THREEDNET-359|L'esportazione da 3DS a GLTF genera un errore di indice|Bug|
|THREEDNET-358|Impossibile rendere la trasparenza del modello|Bug|
### **Pubblico API e modifiche incompatibili arretrate**
Vedere l'elenco di eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non retrocompatibile apportata allo Aspose.3D for .NET. Se hai dubbi su eventuali modifiche elencate, sollevalo sul[Forum di supporto Aspose.3D](https://forum.aspose.com/c/3d/18).
#### **Aggiunge il metodo GetBoundingBox a Aspose.ThreeD. Classe di entità**
**Definizione-C#**

{{< highlight "java" >}}

 /// <summary>

/// Gets the bounding box of current entity in its object space coordinate system.

/// </summary>

public Aspose.ThreeD.Utilities.BoundingBox GetBoundingBox()

{{< /highlight >}}

Gli sviluppatori possono ottenere il riquadro di delimitazione dell'entità nel proprio sistema di coordinate spazio-oggetto.

**Esempio di codice-C#**

{{< highlight "java" >}}

 var box = new Box();

BoundingBox bbox = box.GetBoundingBox(); 

Console.WriteLine(bbox);

{{< /highlight >}}
#### **Aggiunge il tipo enum Aspose.ThreeD.Shading.AlphaSource**
**Definizione-C#**

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
#### **Aggiunge i membri Alpha e AlphaSource alla classe Aspose.ThreeD.Shading.TextureBase**
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

Questi membri vengono aggiunti per renderlo compatibile con la trasparenza della trama in file 3D come U3D/FBX, questi sono supportati anche nel renderer dello Aspose.3D. Dal Aspose.ThreeD.Shading.LambertMaterial/ Aspose.ThreeD.Shading.PhongMaterial/ Aspose.ThreeD.Shading.PbrMaterial ha un TransparencyFactor, ma non è sufficiente per alcuni materiali di trasparenza complessi, dopo 18,3, il materiale può utilizzare il canale alfa per pixel definito nella trama diffusa/albedo.

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
