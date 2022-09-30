---
title: Aspose.3D for Java 18,8 - augusti 2018
type: docs
weight: 50
url: /sv/java/aspose-3d-for-java-18-8-august-2018/
---
{{% alert color="primary" %}} 

Denna sida innehåller utgåvans anteckningar för[Aspose.3D for Java 18,8](https://repository.aspose.com/repo/com/aspose/aspose-3d/18.8/).

{{% /alert %}} 
## **Andra förbättringar och förändringar**

|**Sammanfattning**|**Kategori**|
|:- |:- |
|Exportera glTF filer med dracokomprimering|Ny funktion|
|Optimera minnesförbrukning för mesh-index|Förbättring|
|Använd Aspose.3D med Unity3D|FelComment|
|Läs COLLADA-filer som refererar i samma korg|FelComment|

## **Offentlig API och bakåts oförenliga förändringar**

Vänligen se listan över eventuella ändringar som gjorts i allmänheten API såsom lagts till, bytt namn, avlägsnade eller förlåtna medlemmar samt eventuell icke-back-kompatibel ändring till Aspose.3D for Java 0761333 481. Om du har farhågor om någon förändring som anges, vänligen ta upp det om[Aspose.3D stödforum](https://forum.aspose.com/c/3d).

## **API ändringar:**

**Lagt till en ny getter/setter till klass com.aspose.treed.GLTFSaveOptions:**

{{< highlight "java" >}}

         public bool getDracoCompression();

        public void setDracoCompression(boolean value);

{{< /highlight >}}

Standardvärdet är sant, när detta aktiveras genom att ställa in till true, glTF 2.0-exportören kommer att koda maskorna i format Google Draco.
