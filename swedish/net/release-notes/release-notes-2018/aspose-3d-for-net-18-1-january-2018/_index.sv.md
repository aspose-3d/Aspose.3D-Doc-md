---
title: Aspose.3D for .NET 18,1 - januari 2018
type: docs
weight: 120
url: /sv/net/aspose-3d-for-net-18-1-january-2018/
---
{{% alert color="primary" %}} 

Denna sida innehåller utgåvans anteckningar för[Aspose.3D for .NET 18,1](https://www.nuget.org/packages/Aspose.3D/18.1.0).

{{% /alert %}} 
## **Andra förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|THREEDNET-331|Lägg till ny entitet - Stöd för rektangulär torus|Ny funktion|
|THREEDNET-323|Importera ett dokument ASE|Ny funktion|
|THREEDNET-327|Ogiltig transformation för filen RVM med flera primitive under samma nod.|FelComment|
|THREEDNET-325|RVM fil med slutad cylinder stöds inte.|FelComment|
|THREEDNET-324|Kan inte importera en RVM- fil|FelComment|
### **Offentlig API och bakåts oförenliga förändringar**
Se förteckningen över eventuella ändringar i allmänheten API såsom lagts till, bytt namn, Avlägsnade eller förlåtna medlemmar samt eventuella icke-tillbaka-kompatibla förändringar till Aspose.3D for .NET. Om du har farhågor om någon förändring som anges, vänligen ta upp det om[Aspose.3D stödforum](https://forum.aspose.com/c/3d/18).
#### **Lägger till ASE medlem till Aspose.ThreeD.FileFormat klass**
Detta används för att identifiera inmatningsformatet för filen när du laddar en scen från ström eller filnamn.

**C#**

{{< highlight "java" >}}

 public static readonly Aspose.ThreeD.FileFormat ASE;

{{< /highlight >}}

{{% alert color="primary" %}} 

Aspose.3D kan automatiskt upptäcka om en fils typ är ASE eller andra format, Det behövs vanligtvis inte när du ringer Scene. Öppna metoden.

{{% /alert %}} 

**Urvalskod**

{{< highlight "java" >}}

 Scene scene = new Scene();

scene.Open("test.ase", FileFormat.ASE);

{{< /highlight >}}
#### **Lägger till centerns egenskap till Aspose.ThreeD.A3DOct klass**
Standardvärdet är falskt, om detta är sant, sedan Aspose.3D API kommer att försöka centrera scenen genom att flytta rotnoden.

**C#**

{{< highlight "java" >}}

 Scene scene = new Scene();

scene.Open("test.rvm", new RvmLoadOptions() {CenterScene = true});

{{< /highlight >}}
#### **Lägger till en ny klass Aspose.ThreeD.Enheter.RectangularTorus.**
Det tillåter användaren att placera en parameteriserad rektangulär torus i scenen, Detta kan konverteras till ordinarie mesh/triangelt mesh under att spara scenen till olika filformat som stöds.

**C#**

{{< highlight "java" >}}

 /// <summary>

/// Parameterized rectangular torus.

/// </summary>

public class RectangularTorus : Primitive

{

    /// <summary>

    /// The inner radius of the rectangular torus

    /// Default value is 17

    /// </summary>

    public double InnerRadius { get; set; }

    /// <summary>

    /// The outer radius of the rectangular torus

    /// Default value is 20

    /// </summary>

    public double OuterRadius { get; set; }

    /// <summary>

    /// The height of the rectangular torus.

    /// Default value is 20

    /// </summary>

    public double Height { get; set; }

    /// <summary>

    /// The total angle of the arc, measured in radian.

    /// Default value is PI

    /// </summary>

    public double Arc { get; set; }

    /// <summary>

    /// The start angle of the arc, measured in radian.

    /// Default value is 0

    /// </summary>

    public double AngleStart { get; set; }

    /// <summary>

    /// The radial segments, default value is 10

    /// </summary>

    public int RadialSegments { get; set; }

    /// <summary>

    /// Constructor of <see cref="RectangularTorus"/>

    /// </summary>

    public RectangularTorus();

    /// <summary>

    /// Constructor of <see cref="RectangularTorus"/>

    /// </summary>

    public RectangularTorus(string name);

    /// <summary>

    /// Convert this primitive to <see cref="Mesh"/>

    /// </summary>

    /// <returns></returns>

    public Mesh ToMesh();

}

{{< /highlight >}}

**Provkod:**

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

Den genererade rtorus.obj ser ut som:

![TOD:imageName_Av_Text:](aspose-3d-for-net-18-1-january-2018_1.png)
#### **Exempel**
Kontrollera listan över hjälpämnen som lagts till eller uppdaterats i Wiki-dokumenten Aspose.3D:

1. [Skapa och läsa en existerande scen 3D](/3d/sv/net/create-and-read-an-existing-3d-scene/)
1. [Skapa rektangulär Torus i 3D Scene](/3d/sv/net/create-rectangular-torus-in-3d-scene/)
