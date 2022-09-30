---
title: Aspose.3D for .NET 19,5 Utgivning
type: docs
weight: 80
url: /sv/net/aspose-3d-for-net-19-5-release-notes/
---
{{% alert color="primary" %}} 

Denna sida innehåller utgåvans anteckningar för[Aspose.3D for .NET 19,5](https://www.nuget.org/packages/Aspose.3D/19.5.0)

{{% /alert %}} 
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|THREEDNET-501|Integrera med senaste Dynabic.Meterad|Förbättring|
|THREEDNET-505|Tillåt ändra planets orientering genom att ange ett upp normalt|Förbättring|
|THREEDNET-489|Shadow fungerar inte i Vulkan renderaren|FelComment|
|THREEDNET-504|Draco skapad från STL filen är trasig|FelComment|
### **Offentlig API och bakåts oförenliga förändringar**
Se förteckningen över eventuella ändringar i allmänheten API såsom lagts till, bytt namn, Avlägsnade eller förlåtna medlemmar samt eventuella icke-tillbaka-kompatibla förändringar till Aspose.3D for .NET. Om du har farhågor om någon förändring som anges, vänligen ta upp det om[Aspose.3D stödforum](https://forum.aspose.com/c/3d).
#### **Lagt ny fastighet Radie i klass Aspose.ThreeD.Enheter.Plane**
{{< highlight "java" >}}

 /// <summary>

/// Gets or sets the up vector of the plane, default value is (0, 1, 0), this affects the generation of the plane

/// </summary>

public Vector3 Up { get; set; }

{{< /highlight >}}

Kod för att ange radie per egenskap istället för konstruktorargument:

{{< highlight "java" >}}

 Scene scene = new Scene();

scene.RootNode.CreateChildNode(new Plane() {Up = new Vector3(1, 1, 3)});

//This will generate a plane that has customized orientation

scene.Save("test.obj", FileFormat.WavefrontOBJ);

{{< /highlight >}}
#### **Lagt till ny metod "GetConsumptionCredit" i klass Aspose.ThreeD.Meterad**
{{< highlight "java" >}}

 /// <summary>

/// Gets consumption credit

/// </summary>

/// <returns>consumption quantity</returns>

public static decimal GetConsumptionCredit();

{{< /highlight >}}

` `Får konsumtionskredit för innevarande månad, som används av Dynabic.
