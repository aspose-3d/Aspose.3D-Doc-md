---
title: Aspose.3D for .NET 16.9.0 Utgivning
type: docs
weight: 30
url: /sv/net/aspose-3d-for-net-16-9-0-release-notes/
---
{{% alert color="primary" %}} 

Denna sida innehåller utgåvans anteckningar för[Aspose.3D for .NET 16,9,0](https://www.nuget.org/packages/Aspose.3D/16.9.0).

{{% /alert %}} 
## **Andra förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|THREEDNET-209|Skapa tangent från mesh data.|Ny funktion|
|THREEDNET-208|Normal kartläggning vid rendering.|Ny funktion|
|THREEDNET-182|Export 3D scen till PDF 1,6.|Ny funktion|
|THREEDNET-205|Importera 3D scener från en PDF fil.|Ny funktion|
### **Offentlig API och bakåts oförenliga förändringar**
Se listan för eventuella ändringar i allmänheten API såsom lagts till, bytt namn, Avlägsnade eller förlåtna medlemmar samt eventuella icke-tillbaka-kompatibla förändringar till Aspose.3D for .NET. Om du har farhågor om någon förändring som anges, vänligen ta upp det om[Aspose.3D stödforum](https://forum.aspose.com/c/3d/18).
### **Spara en 3D scen i formatet PDF**
Med den senaste versionen (16.9.0) eller högre kan utvecklare spara alla 3D-filer som stöds i formatet PDF.
#### **Lägger till Aspose.ThreeD. Format.PdfSaveOptions ClassName**
Vi har lagt till PdfSaveOptions klass. Det hjälper till att tillämpa inställning innan du sparar i utgången PDF format.
#### **Lägger till Aspose.ThreeD. Format.PdfLightingScheme/PdfRenderMode Enump**
Utvecklare kan ställa in ett renderingsläge och belysningsschema innan de sparar en 3D scen i formatet PDF.
### **Import 3D Scen från källan PDF**
Använder den senaste versionen (16. 9.0) eller högre, kan utvecklare hämta 3D scener från en indata PDF fil.
#### **Lägger till Aspose.ThreeD. Format.PdfLoadOptions ClassName**
Vi har lagt till PdfLoadOptions klass. Det hjälper till att ladda innehåll från indata PDF-filen. Utvecklare kan använda lösenord för de skyddade PDF-filerna.
#### **Lägger till PDF i formatet Aspose.ThreeD.FileFormat klass**
Vi har lagt till en post av PDF format för lastning och sparande.
#### **Lägger till Aspose.ThreeD. Format.PdfFormat klass**
Vi har lagt till PdfFormat klass. Det hjälper till att manipulera PDF-filer.
### **Lägger till Trianguleringsmetod i Aspose.ThreeD.Entites.PolygonModifier Class.**
Vi har lagt till en annan överbelastning av Triangulate metod i PolygonModifier klassen som tar ett Scene klass objekt som en parameter.
#### **Lägger till två BuildTangentBinormala metoder i Aspose.ThreeD.Enheter.PolygonModifier Class.**
Vi har lagt till två BuildTangentBinormal metoder i PolygonModifier klassen. En metod tar Scene klassobjektet som en parameter och en annan tar Mesh klassobjektet som en parameter.