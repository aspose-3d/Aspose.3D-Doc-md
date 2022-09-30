---
title: Aspose.3D for Java 18.10 - oktober 2018
type: docs
weight: 30
url: /sv/java/aspose-3d-for-java-18-10-october-2018/
---
{{% alert color="primary" %}} 

Denna sida innehåller utgåvans anteckningar för[Aspose.3D for Java 18,0](https://repository.aspose.com/repo/com/aspose/aspose-3d/18.10/).

{{% /alert %}} 
## **Förbättringar och förändringar**


|**Sammanfattning**|**Kategori**|
|:- |:- |
|Stöd for .NET Kärnplattformen|Ny funktion|
|Tillåt användaren att stänga av komprimering när FBX binärfiler|Ny funktion|
|Förbättra FBX importresultat|Förbättring|
|Förbättra FBX Binär skrivprestandande|Förbättring|
|ImportException när du öppnar enorma FBX filer|FelComment|
|Problem med UnitScaleFactor-egenskapen|FelComment|

## **Offentlig API och bakåts oförenliga förändringar**

Vänligen se listan över eventuella ändringar som gjorts i allmänheten API såsom lagts till, bytt namn, avlägsnade eller förlåtna medlemmar samt eventuell icke-back-kompatibel ändring till Aspose.3D for Java 0761333 481. Om du har farhågor om någon förändring som anges, vänligen ta upp det om[Aspose.3D stödforum](https://forum.aspose.com/c/3d).

## **API ändringar:**

**Lagde till medlemmar i klassen 'com.aspose. Threed.FBXSaveOptions':**

{{< highlight "java" >}}

     /**

     * Compression large binary data in the FBX file, default value is true.

     */

    public boolean com.aspose.threed.FBXSaveOptions.getEnableCompression();

    /**

     * Compression large binary data in the FBX file, default value is true.

     */

    public void com.aspose.threed.FBXSaveOptions.setEnableCompression(boolean val);

{{< /highlight >}}





**Provkod:**

{{< highlight "java" >}}

     Scene scene = new Scene("test.fbx");

    FBXSaveOptions opts = new FBXSaveOptions(FileFormat.FBX7500_BINARY);

    opts.setEnableCompression(false);

    scene.save("test.fbx", opts);

{{< /highlight >}}
