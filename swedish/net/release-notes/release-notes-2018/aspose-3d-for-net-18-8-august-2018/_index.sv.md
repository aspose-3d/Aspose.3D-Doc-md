---
title: Aspose.3D for .NET 18,8 - augusti 2018
type: docs
weight: 50
url: /sv/net/aspose-3d-for-net-18-8-august-2018/
---
{{% alert color="primary" %}} 

Denna sida innehåller utgåvans anteckningar för[Aspose.3D for .NET 18,8](https://www.nuget.org/packages/Aspose.3D/18.8.0).

{{% /alert %}} 
## **Andra förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|THREEDNET-409|Exportera glTF filer med dracokomprimering|Ny funktion|
|THREEDNET-401|Använd Aspose.3D med Unity3D|FelComment|
|THREEDNET-413|Läs COLLADA-filer som refererar i samma korg|FelComment|
### **Offentlig API och bakåts oförenliga förändringar**
Se förteckningen över eventuella ändringar i allmänheten API såsom lagts till, bytt namn, Avlägsnade eller förlåtna medlemmar samt eventuella icke-tillbaka-kompatibla förändringar till Aspose.3D for .NET. Om du har farhågor om någon förändring som anges, vänligen ta upp det om[Aspose.3D stödforum](https://forum.aspose.com/c/3d).
### **API ändringar**
#### **Lagt till en ny egenskap i klass Aspose.ThreeD.Formats.GLTFSaveOptions:**
{{< highlight "java" >}}

 	bool DracoCompression{ get;set;}

{{< /highlight >}}

Standardvärdet är sant, när detta aktiveras genom att ställa in till true, glTF 2.0-exportören kommer att koda maskorna i format Google Draco.
