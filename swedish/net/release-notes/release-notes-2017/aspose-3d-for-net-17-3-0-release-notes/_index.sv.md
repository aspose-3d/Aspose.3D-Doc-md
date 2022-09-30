---
title: Aspose.3D for .NET 17.3.0 Utgivning
type: docs
weight: 100
url: /sv/net/aspose-3d-for-net-17-3-0-release-notes/
---
{{% alert color="primary" %}} 

Denna sida innehåller utgåvans anteckningar för[Aspose.3D for .NET 17.3.01](https://www.nuget.org/packages/Aspose.3D/17.3.0).

{{% /alert %}} 
## **Andra förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|THREEDNET-233|Lägg till stöd för att importera Google Draco (.drc) filer.|Ny funktion|
### **Offentlig API och bakåts oförenliga förändringar**
Se förteckningen över eventuella ändringar i allmänheten API såsom lagts till, bytt namn, Avlägsnade eller förlåtna medlemmar samt eventuella icke-tillbaka-kompatibla förändringar till Aspose.3D for .NET. Om du har farhågor om någon förändring som anges, vänligen ta upp det om[Aspose.3D stödforum](https://forum.aspose.com/c/3d/18).
#### **Lägger till Draco formatpost i Aspose.ThreeD.FileFormat klass**
Detta utgivare av Aspose.3D for .NET API har lagt till stöd för import av Google 076143. 481(. a) ärenden. Utvecklare kan importera en Google Draco fil, och sedan spara den i alla stöds 3D format.

Detta kodexempel visar hur man importerar en fil Google Draco till Aspose.3D API:

**.NET, C#**

{{< highlight "java" >}}

 // Initialize a Scene class object

Scene scene = new Scene();

// load an existing 3D document

scene.Open("document.drc", FileFormat.Draco);

{{< /highlight >}}
