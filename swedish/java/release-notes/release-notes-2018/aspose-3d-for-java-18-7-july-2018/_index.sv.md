---
title: Aspose.3D for Java 18,7 – juli 2018
type: docs
weight: 60
url: /sv/java/aspose-3d-for-java-18-7-july-2018/
---
{{% alert color="primary" %}} 

Denna sida innehåller utgåvans anteckningar för[Aspose.3D for Java 18,7](https://repository.aspose.com/repo/com/aspose/aspose-3d/18.7/).

{{% /alert %}} 
## **Andra förbättringar och förändringar**

|**Sammanfattning**|**Kategori**|
|:- |:- |
|Lägg till Draco 2.2 importstöd|Ny funktion|
|Lägg till Draco 2.2 exportstöd|Ny funktion|
|Importera glTF filer med dracokomprimering|Ny funktion|

## **Offentlig API och bakåts oförenliga förändringar**
Vänligen se listan över eventuella ändringar som gjorts i allmänheten API såsom lagts till, bytt namn, avlägsnade eller förlåtna medlemmar samt eventuell icke-back-kompatibel ändring till Aspose.3D for Java 0761333 481. Om du har farhågor om någon förändring som anges, vänligen ta upp det om[Aspose.3D stödforum](https://forum.aspose.com/c/3d).

## **API ändringar:**

**3 medlemmar avlägsnade från klassen com.aspose.treed.Property:**

{{< highlight "java" >}}

     public void com.aspose.threed.Property.setExtraData(java.lang.String);

    public java.lang.String com.aspose.threed.Property.getExtraData();

    public int com.aspose.threed.Property.getFlags();

{{< /highlight >}}

Dessa tas bort för att synkronisera ändringarna från .NET version. (De är planerade att tas bort sedan Aspose.3D for .NET 18.2).

**1 egenskap läggs till i klass com.aspose.treed.ObjLoadOptions:**

{{< highlight "java" >}}

     public boolean com.aspose.threed.ObjLoadOptions.getNormalizeNormal();

    public void com.aspose.threed.ObjLoadOptions.setNormalizeNormal(boolean);

{{< /highlight >}}

Får eller ställer in om den normala vektorn ska normaliseras under laddningen. Standardvärdet är sant.

**Provkod:**

{{< highlight "java" >}}

         Scene scene = new Scene();

        ObjLoadOptions opt = new ObjLoadOptions();

        opt.setNormalizeNormal(false);

        scene.open("test.obj", opt);

{{< /highlight >}}

Detta kommer att ladda obj- filen och lämna de normala vektorerna onormala, Den gamla versionen normaliserar de vanliga vektorerna när obj-filen laddas.
