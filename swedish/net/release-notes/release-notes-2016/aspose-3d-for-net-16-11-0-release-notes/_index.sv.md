---
title: Aspose.3D for .NET 16.11.0 Utgivning
type: docs
weight: 20
url: /sv/net/aspose-3d-for-net-16-11-0-release-notes/
---
{{% alert color="primary" %}} 

Denna sida innehåller utgåvans anteckningar för[Aspose.3D for .NET 16,11,0](https://www.nuget.org/packages/Aspose.3D/16.11.0).

{{% /alert %}} 
## **Andra förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|THREEDNET-219|Rikt/punktsljus i rendering.|Ny funktion|
|THREEDNET-218|Lägg till ett nytt gränssnitt för att tillåta användaren att exportera beroenden till filsystemet.|Ny funktion|
|THREEDNET-217|Lägg till stöd för att exportera texten/binär glTF.|Ny funktion|
|THREEDNET-215|Lägg till stöd för att importera binären glTF.|Ny funktion|
|THREEDNET-211|Lägg till stöd för att importera textbaserade glTF.|Ny funktion|
### **Offentlig API och bakåts oförenliga förändringar**
Se förteckningen över eventuella ändringar i allmänheten API såsom lagts till, bytt namn, Avlägsnade eller förlåtna medlemmar samt eventuella icke-tillbaka-kompatibla förändringar till Aspose.3D for .NET. Om du har farhågor om någon förändring som anges, vänligen ta upp det om[Aspose.3D stödforum](https://forum.aspose.com/c/3d/18).
### **Lägger till Aspose.ThreeD. Format.GLTFLoadOptions ClassName**
Vi har lagt till GLTFLoadOptions klass. Den definierar inställningar på att ladda en glTF-fil.
### **Lägger till Aspose.ThreeD. Format.GLTFSaveOptions ClassName**
Vi har lagt till GLTFSaveOptions klass. Det definierar inställningar för att spara en glTF fil.
### **Lägger till Aspose.ThreeD.Användare.DummyFileSystem ClassName**
Det kommer att ignorera alla beroenden medan man sparar scenen med hjälp av spara alternativklasser.
### **Lägger till Aspose.ThreeD.Användare.LokalfilSystem ClassName**
Alla beroenden skrivs till det verkliga filsystemet, detta är standardvärdet för varje sparalternativklasser, Utvecklare kan använda detta för att omdirigera beroenden till en annan korg.
### **Lägger till Aspose.ThreeD.Användningar.MinneFileSystem ClassName**
MemoryFileSystems klass avskräcker skrivningen av beroenden, t.ex. få filens innehåll "test.mtl".
### **Lägger till tillägg och GLTF Format poster i Aspose.ThreeD.FileFormat Class.**
Vi har lagt till en tillägg fastighet och GLTF (GLTF och GLTF_Bin) Formatposter för lastning och sparande.
#### **Lägger till en tilläggsegenskap i Aspose.ThreeD.FileFormatType ClassName**
Vi har lagt till en Extensions egenskap i FileFormatType-klassen för att få filformatets tilläggsnamn.
### **Lägger till egenskapen FileSystem i Aspose.ThreeD.Formats.IOConfig**
Vi har lagt till en FileSystem i IOConfig-klassen för att skriva beroenden.
### **Lägger till enhetsmetod i Aspose.ThreeD.Nod klass**
En genväg för att lägga till en enhet i en nod
