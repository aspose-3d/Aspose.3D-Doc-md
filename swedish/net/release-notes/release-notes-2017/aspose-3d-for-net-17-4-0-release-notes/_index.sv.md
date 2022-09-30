---
title: Aspose.3D for .NET 17.4.0 Utgivningsmeddelanden
type: docs
weight: 90
url: /sv/net/aspose-3d-for-net-17-4-0-release-notes/
---
{{% alert color="primary" %}} 

Denna sida innehåller utgåvans anteckningar för[Aspose.3D for .NET 17.4.00](https://www.nuget.org/packages/Aspose.3D/17.4.0).

{{% /alert %}} 
## **Andra förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|THREEDNET-235|Lägg till stöd för att exportera 3D modeller till Google Draco (.drc) format.|Ny funktion|
|THREEDNET-237|Förbättra kamerarörelsen i ortografisk projektionsläge.|Förbättring|
|THREEDNET-238|Lägg till stöd för att zooma ut kameran|Förbättring|
### **Offentlig API och bakåts oförenliga förändringar**
Se förteckningen över eventuella ändringar i allmänheten API såsom lagts till, bytt namn, Avlägsnade eller förlåtna medlemmar samt eventuella icke-tillbaka-kompatibla förändringar till Aspose.3D for .NET. Om du har farhågor om någon förändring som anges, vänligen ta upp det om[Aspose.3D stödforum](https://forum.aspose.com/c/3d/18).
#### **Spara en 3D modell i Google Draco (.drc)**
Den senaste utgåvan av Aspose.3D for .NET API har lagt till stöd för att exportera 3D modeller till Google Draco (. drc) format. Utvecklare kan importera alla stödda 3D filer, och sedan spara i ett format Google Draco.

Detta kodexempel visar hur man exporterar en 3D modell till ett filformat Google Draco:

**.NET, C#**

{{< highlight "java" >}}

 //Create a new scene

var s = new Scene();

//Create a sphere object and attach it to the scene

s.RootNode.CreateChildNode("sphere", new Sphere());

//save it to file using draco format

s.Save("sphere.drc", FileFormat.Draco);

{{< /highlight >}}
#### **Lägger till Aspose.ThreeD. Format.Draco.DracoCompressionLevel EnumName**
DracoCompressionLevel Enum hjälper till att definiera en kompressionsnivå innan man sparar en 3D modell i Google Draco (. drc) format.

Följande fullständiga kod för Enum visar olika kompressionsnivåer med beskrivning:

**.NET, C#**

{{< highlight "java" >}}

 public enum DracoCompressionLevel

{

    /// <summary>

    /// No compression, this will result in the minimum encoding time.

    /// </summary>

    NoCompression,

    /// <summary>

    /// Encoder will perform a compression as quickly as possible.

    /// </summary>

    Fast,

    /// <summary>

    /// Standard mode, with good compression and speed.

    /// </summary>

    Standard,

    /// <summary>

    /// Encoder will compress the scene optimally, which may takes longer time to finish.

    /// </summary>

    Optimal

}

{{< /highlight >}}
### **Lägger till Aspose.ThreeD. Format.Draco.DracoSaveOptions ClassName**
DracoSaveOptions klass tillåter utvecklare att applicera inställningar innan de sparar en 3D modell i Google 071 6123481 (. drc) format.

Följande fullständiga kod för klassen visar alla egenskaper med beskrivning:

**.NET, C#**

{{< highlight "java" >}}

 /// <summary>

/// Quantization bits for position

/// </summary>

public int PositionBits { get; set; }

/// <summary>

/// Quantization bits for texture coordinate

/// </summary>

public int TextureCoordinateBits { get; set; }

/// <summary>

/// Quantization bits for vertex color

/// </summary>

public int ColorBits { get; set; }

/// <summary>

/// Quantization bits for normal vectors

/// </summary>

public int NormalBits { get; set; }

/// <summary>

/// Compression level

/// </summary>

public DracoCompressionLevel CompressionLevel { get; set; }

{{< /highlight >}}
#### **Lägger till Aspose.ThreeD. Format.DracoFormat klass**
Detta.**Koda**Metod i DracoFormat klassen gör att utvecklare kan koda en enda mesh istället för hela scenen, vilket är mer effektivt.

Följande fullständiga kod för klassen visar kodningsmetod med beskrivning:

**.NET, C#**

{{< highlight "java" >}}

 /// <summary>

/// Encode the mesh to Draco mesh raw data

/// </summary>

/// <param name="mesh"></param>

/// <param name="options"></param>

/// <returns></returns>

public byte[]Encode(IMeshConvertible mesh, DracoSaveOptions options = null);

{{< /highlight >}}
#### **Koda en mask i Google Draco (.drc) Format**
Draco-filen har inte stöd för hierarkisk scen, var och en. Drc-filen representerar en mesh, så att spara scenen kommer att sammanfoga hela scenen till en enda mesh, vilket kan förlora information.

Detta kodexempel visar hur man kodar en mesh i Google Draco (.drc) format:

**.NET, C#**

{{< highlight "java" >}}

 //Create a sphere

var mesh = new Sphere();

// Encode the sphere to Google Draco raw data using optimal compression level.

var b = FileFormat.Draco.Encode(mesh,

    new DracoSaveOptions() {CompressionLevel = DracoCompressionLevel.Optimal});

//Save the raw bytes to file

File.WriteAllBytes("sphere.drc", b);

{{< /highlight >}}
#### **Lägger till roteringMode medlem till Aspose.ThreeD.Enheter.Frustum (Basklass för kamera och ljus)**
Standardvärdet är RotationMode.FixedTarget, gör det kompatibelt med gammal kod i realtid rendering. Om Frustums rotationsläge är FixedTarget, orienteringen av frustumen anges av dess egenskap LookAt som är en absolut position i världen, i detta läge kan utvecklare alltid få olika egenskaper Riktning när positionen ändras.

Om rotationsläget är FixedDirection, frustum kommer inte längre att titta på ett mål, men behålla samma riktning (specificerad av sin egenskap av riktning) i förhållande till sin position, detta är användbart för att utforma verktyg som CAD eller FPS-spel, i detta läge kan utvecklare alltid få olika egenskaper LookAt när dess position ändras.

Det här kodexemplet visar hur man anger rotationsläget för en kamera:

**.NET, C#**

{{< highlight "java" >}}

 Camera camera = new Camera();

camera.RotationMode = RotationMode.FixedDirection;

{{< /highlight >}}
#### **Lägger till förstoringsmedlem till Aspose.ThreeD.Enheter.Kamerklass**
Standardvärdet är (1, 1), Ändra detta värde kan göra de återgivna bildskalorna i horisontell/vertikal riktning i ortografisk kamera.

Det här kodexemplet visar hur man anger rotationsläget för en kamera:

**.NET, C#**

{{< highlight "java" >}}

 /// <summary>

/// Gets or sets the magnification used in orthographic camera

/// </summary>

public Vector2 Magnification { get;set; }

.................................................

Camera camera = new Camera();

camera.Magnification = new Vector2(2, 2);

{{< /highlight >}}
