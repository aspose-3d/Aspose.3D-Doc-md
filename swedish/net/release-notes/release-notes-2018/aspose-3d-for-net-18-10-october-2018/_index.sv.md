---
title: Aspose.3D for .NET 18.10 - oktober 2018
type: docs
weight: 30
url: /sv/net/aspose-3d-for-net-18-10-october-2018/
---
{{% alert color="primary" %}} 

Denna sida innehåller utgåvans anteckningar för[Aspose.3D for .NET 18,0](https://www.nuget.org/packages/Aspose.3D/18.10.0).

{{% /alert %}} 
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|THREEDNET-434|Stöd for .NET Kärnplattformen|Ny funktion|
|THREEDNET-431|Tillåt användaren att stänga av komprimering när FBX binärfiler|Ny funktion|
|THREEDNET-424|Förbättra FBX importresultat|Förbättring|
|THREEDNET-432|Förbättra FBX Binär skrivprestandande|Förbättring|
|THREEDNET-428|ImportException när du öppnar enorma FBX filer|FelComment|
|THREEDNET-429|Problem med UnitScaleFactor-egenskapen|FelComment|
### **Offentlig API och bakåts oförenliga förändringar**
Se förteckningen över eventuella ändringar i allmänheten API såsom lagts till, bytt namn, Avlägsnade eller förlåtna medlemmar samt eventuella icke-tillbaka-kompatibla förändringar till Aspose.3D for .NET. Om du har farhågor om någon förändring som anges, vänligen ta upp det om[Aspose.3D stödforum](https://forum.aspose.com/c/3d).
### **API ändringar**
#### **Lagt till medlemmar i klass Aspose.ThreeD.Formats.FBXSaveOptions:**
{{< highlight "java" >}}

         /// <summary>

        /// Compression large binary data in the FBX file, default value is true.

        /// </summary>

        public bool EnableCompression{ get;set;}

{{< /highlight >}}

**Provkod:**

{{< highlight "java" >}}

         Scene scene = new Scene("test.fbx");

        scene.Save("test.fbx", new FBXSaveOptions(FileFormat.FBX7500ASCII) {EnableCompression = false});

{{< /highlight >}}
