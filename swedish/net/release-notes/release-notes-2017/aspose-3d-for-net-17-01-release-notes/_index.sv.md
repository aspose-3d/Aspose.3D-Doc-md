---
title: Aspose.3D for .NET 17.01 Utgivningsmeddelanden
type: docs
weight: 120
url: /sv/net/aspose-3d-for-net-17-01-release-notes/
---
{{% alert color="primary" %}} 

Denna sida innehåller utgåvans anteckningar för[Aspose.3D for .NET 17,1,0](https://www.nuget.org/packages/Aspose.3D/17.1.0).

{{% /alert %}} 
## **Andra förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|THREEDNET-227|Lägg till stöd för att importera PLY modeller.|Ny funktion|
### **Offentlig API och bakåts oförenliga förändringar**
Se förteckningen över eventuella ändringar i allmänheten API såsom lagts till, bytt namn, Avlägsnade eller förlåtna medlemmar samt eventuella icke-tillbaka-kompatibla förändringar till Aspose.3D for .NET. Om du har farhågor om någon förändring som anges, vänligen ta upp det om[Aspose.3D stödforum](https://forum.aspose.com/c/3d/18).
#### **Lägger till en PLY-formatpost i Aspose.ThreeD.FileFormat klass**
Vi har lagt till en PLY (Polygon File Format) posten för import ändamål.
#### **Lägger till Aspose.ThreeD. Format.PLY.PlyLoadOptions ClassName**
Den anger belastningsinställningar för att ladda en PLY modell i Aspose.3D API. Denna laddningsklass har bara en FlipCoordinateSystem- egenskap, som också finns i laddningsalternativ klasser av andra filformat.
#### **Lägger till Aspose.ThreeD.GlobalTransform ClassName**
Klassen GlobalTransform ger exakt samma gränssnitt som Transform men alla dess egenskaper är skrivskyddade. Den är användbar för den globala omvandlingen.
#### **Lägger till en GlobalTransform egenskap till Aspose.ThreeD.Node Class.**
Det tillåter att komma åt nodens globala transformation. Detta är användbart för att omvandla scenen till användarens egna filformat.
#### **Lägger till Polygons fastighet till Aspose.ThreeD.Enheter.Mesh Klass**
Det tillåter att få alla polygoner inuti mesh, varje polygon är en array av polygon vertex index. Innan denna egenskap, måste vi använda foreach syntax för att räkna upp varje polygon som är ineffektiv.
#### **Tar bort CreateStream medlem från Aspose.ThreeD.Formats.IOConfig klass**
Detta markerades som föråldrat i version 16.11.0, det nya gränssnittet FileSystem introducerades i version 16.11.0 som ger fler extensibiliteter.
