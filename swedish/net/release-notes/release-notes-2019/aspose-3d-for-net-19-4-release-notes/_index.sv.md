---
title: Aspose.3D for .NET 19,4 Utgivning
type: docs
weight: 90
url: /sv/net/aspose-3d-for-net-19-4-release-notes/
---
{{% alert color="primary" %}} 

Denna sida innehåller utgåvans anteckningar för[Aspose.3D for .NET 19,4](https://www.nuget.org/packages/Aspose.3D/19.4.0)

{{% /alert %}} 
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|THREEDNET-471|XPath- liknande objekt adresseringsmetoder|Ny funktion|
|THREEDNET-483|Stöd för format VRML|Ny funktion|
|THREEDNET-493|Tillagd vulkan renderingsstöd i .NET Kärnversionen|Ny funktion|
|THREEDNET-496|FBX7500Binarisexportfrågor|FelComment|
### **Offentlig API och bakåts oförenliga förändringar**
Se förteckningen över eventuella ändringar i allmänheten API såsom lagts till, bytt namn, Avlägsnade eller förlåtna medlemmar samt eventuella icke-tillbaka-kompatibla förändringar till Aspose.3D for .NET. Om du har farhågor om någon förändring som anges, vänligen ta upp det om[Aspose.3D stödforum](https://forum.aspose.com/c/3d).
#### **Lagt ny fastighet Radie i klass Aspose.ThreeD.Enheter.Sphere.**
{{< highlight "java" >}}

 /// <summary>

/// Gets or sets the radius of the sphere.

/// </summary>

public double Radius { get; set; }

{{< /highlight >}}

Kod för att ange radie per egenskap istället för konstruktorargument:

{{< highlight "java" >}}

 Scene scene = new Scene();

scene.RootNode.CreateChildNode(new Sphere() {Radius = 10});

scene.Save("sphere.obj", FileFormat.WavefrontOBJ);

{{< /highlight >}}
#### **Lagt till nytt filformat VRML i klass Aspose.ThreeD.FileFormat och Aspose.ThreeD.FileFormatTypeName**
{{< highlight "java" >}}

 /// <summary>

/// The Virtual Reality Modeling Language

/// </summary>

public static readonly FileFormat VRML;

{{< /highlight >}}

Aspose.3D kan automatiskt detektera VRML format, så FileFormat oftast ignoreras i Öppna metoden. Provkod:

{{< highlight "java" >}}

 Scene scene = new Scene();

scene.Open("test.wrl");

{{< /highlight >}}
