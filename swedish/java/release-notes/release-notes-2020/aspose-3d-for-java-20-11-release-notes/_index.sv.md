---
title: Aspose.3D for Java 20.11 Utgivning
type: docs
weight: 6
url: /sv/java/aspose-3d-for-java-20-11-release-notes/
---
{{% alert color="primary" %}}

Denna sida innehåller release anteckningar för Aspose.3D for Java 20.11.

{{% /alert %}}
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|THREEDNET-747 |Rendera kantlinjerna för CAD typer i webben renderare.|Felrättning|
|THREEDNET-748 |Förbättra belysningen i webben återgivning|Felrättning|
|THREEDNET-755 |Modell attribut stöds inte i några FBX 6.1 filer.|Felrättning|
|THREEDNET-757 |PLY fil med int64-egenskap stöds inte.|Felrättning|
|THREEDNET-756 |3MF fil som exporteras med hjälp av senaste standard kan inte öppnas.|Felrättning|
|THREEDNET-758 |FBX 6.0 fil kan inte importeras.|Felrättning|
|THREEDNET-760 |Förbättra kompatibiliteten för ASE filer|Felrättning|
|THREEDNET-761 |Tillåt ange kodningen för textbaserade 3D- filer.|Förbättring|
|THREEDNET-762 |Exportera scen till HTML med vår senaste renderare.|Ny funktion|
|THREEDNET-763 |Lägg till stöd för icke-standard kollada exporterat av okänd exportör.|Förbättring|
|THREEDNET-765 |Optimera laddningsprestanda för binär PLY-fil 0761031|Förbättring|
|THREEDNET-768 |Binär STL-fil som exporteras av Rhinoceros kan inte importeras.|Felrättning|
|THREEDNET-769 |Lägg till stöd för förbindelserna FBX 6.0|Felrättning|
|TRHEEDNET-770 |Felaktigt skrivtecken i filen FBX orsakar att Aspose.3D inte importerade.|Felrättning|
|THREEDNET-771 |Lägg till stöd för inbäddningsdata i FBX|Felrättning|


## API ändringar ##


Den största förändringen i den här versionen är den exporterade filen HTML5 kommer inte längre att använda den gamla renderaren.

Istället används en WebAställe-baserad renderare för återgivning.

Många fel har rättats i den här versionen.

### Lagt till ny egenskap i klassen com.aspose.treed.VertexElementUserData:

{{< highlight "java" >}}

    /**
     * Gets the indices data
     */
    @Override
    public List<Integer> getIndices();

{{< /highlight >}}

Denna egenskap läggs till så fbx-filer innehåller indicerade användardata kan importeras korrekt.


### Lagt till ny egenskap i klassen com.aspose.3reed.IOConfig:

{{< highlight "java" >}}

    /**
     * Gets the default encoding for text-based files.
     * Default value is null which means the importer/exporter will decide which encoding to use.
     */
    public Charset getEncoding();
    
    /**
     * Sets the default encoding for text-based files.
     * Default value is null which means the importer/exporter will decide which encoding to use.
     * @param value New value
     */
    public void setEncoding(Charset value);

{{< /highlight >}}

Detta används för att åsidosätta standardkodningen under import/export. så att du manuellt kan styra kodningen av textbaserade format.