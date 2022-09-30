---
title: Aspose.3D for .NET 16.12.0 Utgivning
type: docs
weight: 10
url: /sv/net/aspose-3d-for-net-16-12-0-release-notes/
---
{{% alert color="primary" %}} 

Denna sida innehåller utgåvans anteckningar för[Aspose.3D for .NET 16,12,0](https://www.nuget.org/packages/Aspose.3D/16.12.0).

{{% /alert %}} 
## **Andra förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|THREEDNET-223|Lägg till stöd för att importera DXF.|Ny funktion|
|THREEDNET-224|Lägg till ett uppmätt licensnyckelsystem.|Ny funktion|
|THREEDNET-226|Kan inte extrahera 3D data från en PDF.|FelComment|
### **Offentlig API och bakåts oförenliga förändringar**
Se förteckningen över eventuella ändringar i allmänheten API såsom lagts till, bytt namn, Avlägsnade eller förlåtna medlemmar samt eventuella icke-tillbaka-kompatibla förändringar till Aspose.3D for .NET. Om du har farhågor om någon förändring som anges, vänligen ta upp det om[Aspose.3D stödforum](https://forum.aspose.com/c/3d/18).
### **Lägger till en DXF-formatpost i Aspose.ThreeD.FileFormat klass**
Vi har lagt till en DXF (Graphic Image Format) posten för import ändamål. Auto-detektera för filen DXF stöds, så oftast behöver utvecklare inte manuellt ange detta filformat när du öppnar en DXF fil (med Scene klass).
### **Lägger till Aspose.ThreeD.Meterad klass**
Vi har lagt till Metered klass. Det tillåter utvecklare att låsa upp utvärderingsbegränsningar av Aspose.3D API samt spåra och underhålla 076123488 1 körkort. Den övervakar också regelbunden användning av Aspose.3D API. För att tillämpa det mäterade licensieringssystemet kan utvecklare skapa ett objekt i Metered-klassen och kalla den SetMeteredKey-metoden. SetMeteredKey-metoden tar två strängparametrar som offentliga och privata nycklar. Våra kunder kan få offentliga och privata nycklar från Aspose.
