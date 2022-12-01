---
title: Aspose.3D for .NET 17,12 – december 2017
type: docs
weight: 10
url: /sv/net/aspose-3d-for-net-17-12-december-2017/
---
{{% alert color="primary" %}} 

Denna sida innehåller utgåvans anteckningar för[Aspose.3D for .NET 17,2](https://www.nuget.org/packages/Aspose.3D/17.12.0).

{{% /alert %}} 
## **Andra förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|THREEDNET-304|Lägg till stöd för att exportera RVM (AVEVA PDMS)|Ny funktion|
|THREEDNET-312|Lägg till korthandsväg till skalningsgeometrier|Förbättring|
|THREEDNET-314|Lägg till stöd för att exportera anpassade egenskaper / ID till noder i GLTF format.|Förbättring|
### **Offentlig API och bakåts oförenliga förändringar**
Se förteckningen över eventuella ändringar i allmänheten API såsom lagts till, bytt namn, Avlägsnade eller förlåtna medlemmar samt eventuella icke-tillbaka-kompatibla förändringar till Aspose.3D for .NET. Om du har farhågor om någon förändring som anges, vänligen ta upp det om[Aspose.3D stödforum](https://forum.aspose.com/c/3d/18).
#### **Lägger till egenskapen SaveExtra till Aspose.ThreeD.Formats.GLTFSaveOptions klass**
Standardvärdet på egenskapen SaveExtras är falskt, om du vill ha Aspose.3D for .NET API för att exportera anpassade egenskaper av objektet, Du kan tilldela det till sann.

**C#**

{{< highlight "java" >}}

 public bool SaveExtras{ get;set;}

{{< /highlight >}}

{{% alert color="primary" %}} 

De anpassade egenskaperna sparas i ett "extra" fält på grund av glTF's specifikation. Ett kodexempel beskrivs nedan.

{{% /alert %}}
#### **Lägger till tre medlemmar till Aspose.ThreeD.A3DObjekt**
Ta bortProperty, HämtaProperty, SetProperty är en uppsättning short-handed metoder för att manipulera anpassade egenskaper för objektet. De gamla metoderna som FindProperty och CreateDynamicProperty är alltför för vidare och planeras att tas bort i framtiden. De anpassade egenskaperna stöds av FBX/glTF (Alla versioner).

**C#**

{{< highlight "java" >}}

 public bool RemoveProperty(string property)

public object GetProperty(string property)

public void SetProperty(string property, object value)

{{< /highlight >}}

**Provkod:**

**C#**

{{< highlight "java" >}}

 Scene scene = new Scene();

var box = scene.RootNode.CreateChildNode("box", new Box());

box.SetProperty("obj-id", "box-id");

scene.Save("test.fbx", FileFormat.FBX7400ASCII);

scene.Save("test.gltf", new GLTFSaveOptions(FileFormat.GLTF){SaveExtras = true});

scene.Save("test-2.gltf", new GLTFSaveOptions(FileFormat.GLTF2){SaveExtras = true});

{{< /highlight >}}

Denna kod kommer att spara scenen med de anpassade egenskaperna i FBX, glTF och glTF 2,0.
#### **Lägger till två medlemmar till Aspose.ThreeD.Enheter.PolygonModifier klass**
Dessa medlemmar är praktiska, om utvecklare inte vill ändra nodens transformation men vill skala geometrierna och endast tillämpas på geometrier.

**C#**

{{< highlight "java" >}}

 public static void Scale(Aspose.ThreeD.Scene scene, Aspose.ThreeD.Utilities.Vector3 scale)

public static void Scale(Aspose.ThreeD.Node node, Aspose.ThreeD.Utilities.Vector3 scale)

{{< /highlight >}}

**Provkod:**

**C#**

{{< highlight "java" >}}

 // scale the model in huge-scene.obj by 0.01 and save it to another file:

Scene scene = new Scene("huge-scene.obj");

PolygonModifier.Scale(scene, new Vector3(0.01));

scene.Save("scaled-scene.obj", FileFormat.WavefrontOBJ);

{{< /highlight >}}
#### **Lägger till FindNode- metoden till Aspose.ThreeD.Node klass**
Detta är en praktisk metod för att hitta en barnnod med namnet, det kommer att returnera noll om inte kunde hitta en nod.

**C#**

{{< highlight "java" >}}

 Scene scene = new Scene();

scene.RootNode.CreateChildNode("child", new Box());

Node child = scene.RootNode.FindNode("child");

{{< /highlight >}}
#### **Exempel**
Kontrollera listan över hjälpämnen som lagts till eller uppdaterats i Wiki-dokumenten Aspose.3D:

1. [Manipulera anpassade egenskaper för en 3D Scene](/3d/sv/net/manipulate-custom-properties-of-a-3d-scene/)
1. [Skala geometrier för en 3D Scene](/3d/sv/net/scale-geometries-of-a-3d-scene/)
