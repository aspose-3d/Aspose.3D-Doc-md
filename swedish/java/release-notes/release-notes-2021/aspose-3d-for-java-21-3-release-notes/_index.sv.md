---
title: Aspose.3D for Java 21,3 Utgivning
type: docs
weight: 10
url: /sv/java/aspose-3d-for-java-21-3-release-notes/
---
{{% alert color="primary" %}}

Denna sida innehåller release anteckningar för Aspose.3D for Java 21.3.

{{% /alert %}}
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|THREEDNET-847 |Lägg till stöd för punktmoln i glb|Ny funktion|
|THREEDNET-830 |Tillhandahålla låg nivåsmask API för webben render.|Förbättring|
|THREEDNET-838 |Exportera 2. 5D topografi med färg till en fil|Förbättring|
|THREEDNET-849 |Lägg till byte[ 4] stöd i export glTF|Förbättring|
|THREEDNET-832 |Implementera gizmos för ljus i webben rendering|Förbättring|
|THREEDNET-833 |Implementera gizmo för kamera i webb rendering|Förbättring|
|THREEDNET-842 |Lägg till stöd för UV- tolkning i FBX|Förbättring|
|THREEDNET-852 |Enheter återgivare arkitektur för webb återgivning|Uppgifter|
|THREEDNET-836 |Uppdatera spara / ladda alternativ klassnamn.|Uppgifter|
|THREEDNET-858 |Vissa obj-filer återges inte helt i webben renderare.|Felrättning|
|THREEDNET-859 |X-filer med okänd animationsstruktur kan inte importeras.|Felrättning|
|THREEDNET-861 |Kan inte importera X-filer med FVF- data|Felrättning|
|THREEDNET-860 |Kan inte importera X-filer med flera material med enstaka masker|Felrättning|
|THREEDNET-839 |FBX fil med ConstraintParent stöds inte.|Felrättning|
|THREEDNET-841 |Vissa gamla FBX filer innehåller form avsnitt under modell stöds inte.|Felrättning|
|THREEDNET-840 |ASCII FBX Fil med FilId misslyckades importera.|Felrättning|
|THREEDNET-844 |API kastar ett undantag när du ställer in en giltig licens i .NET Core|Felrättning|
|THREEDNET-843 |API anger inte en giltig licens - kasta undantag i .NET Kärnprojektet|Felrättning|
|THREEDNET-848 |Vissa punktmoln kan inte exporteras till drc|Felrättning|
|THREEDNET-854 |Aspose.3D kraschade vid import några collada-filer med felaktiga materialdefinitioner.|Felrättning|


## API ändringar ##


Denna version är huvudsakligen en felfix-version, fixad en massa fel, och förbättrade mycket kompatibilitet för FBX, Collada, DirectX X-filer.


Bara några mindre ändringar API.

### Lagt till ny datatyp i klass `com.aspose.threed.VertexFieldDataType`:

{{< highlight "java" >}}

    /**
     * Type of byte[4], can be used to represent color with less memory consumption.
     */
    public static final int BYTE_VECTOR4;

{{< /highlight >}}

VertexElementVertexColor i com. Förmodligen. Tre. Geometri kommer att kodas som ett 4 bytes heltal med typ VertexFieldDataType. BYTE_VECTOR4.

Detta kan minska den slutliga genererade fil mycket i glTF/glb som används vertex färg, mycket användbart för kodning punktmoln.

Och från denna version, com.aspose.treed.PointCloud stöds i glTF/glb öppna och spara.



### Lagt till medlemmar i klass `com.aspose.threed.BoundingBox`


{{< highlight "java" >}}

    /**
     * The size of the bounding box
     */
    public Vector3 getSize();
  
    /**
     * The center of the bounding box.
     */
    public Vector3 getCenter();

{{< /highlight >}}

Nu är det lättare att få storleken och mittpunkten i den avgränsande rutan, dessa egenskaper endast gör mening när BoundingBox är ändlig.

