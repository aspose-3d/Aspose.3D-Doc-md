---
title: Aspose.3D for Java 21,4 Utgivning
type: docs
weight: 9
url: /sv/java/aspose-3d-for-java-21-4-release-notes/
---
{{% alert color="primary" %}}

Denna sida innehåller release anteckningar för Aspose.3D for Java 21.4.

{{% /alert %}}
## **Förbättringar och förändringar**
|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|THREEDNET-864 |Implementera egenskapen FileStream för texture Class för att ladda bild från en ström.|Förbättring|
|THREEDNET-867 |Stor obj-fil tar mycket tid att ladda|Förbättring|
|THREEDNET-865 |Lägg till Autodesk Navisworks kompatibelt material för RVM format.|Förbättring|
|THREEDNET-874 |Lägg till stöd för senaste RVM format.|Förbättring|
|THREEDAPP-94 |Förbättrad prestanda för webben renderare|Förbättring|
|THREEDNET-851 |Tillåt använda extern implementering av Draco kodare.|Förbättring|
|THREEDNET-876 |Förbättra inbyggd Draco encoder / avkodare prestanda.|Förbättring|
|THREEDNET-862 |Konverterad glb-fil kan inte öppnas av tredje party-verktyg.|Felrättning|
|THREEDNET-863 |Omvandling från USDZ till STL misslyckar|Felrättning|
|THREEDNET-866 |FBX till gltf/glb ExportException: Objekttyp Aspose.ThreeD. -Det är det. Vector3 stöds inte|Felrättning|
|THREEDNET-873 |Collada exporteras av Frosty Suite kan inte importeras.|Felrättning|
|THREEDNET-872 |Collada exporteras av mixer/lego verktyg kan inte importeras.|Felrättning|
|THREEDNET-871 |Vissa zippade 3D filer kan inte öppnas av Aspose.3D|Felrättning|
|THREEDNET-869 |Några STL filer erkänns inte.|Felrättning|
|THREEDAPP-114 |Binära STL-filer utan ett uttryckligt binärhuvud kan inte öppnas.|Felrättning|


## API ändringar ##


Denna version är huvudsakligen en felfix-version, fixad en massa fel, och förbättrade många frågor om kompatibilitet och prestanda för FBX, Collada, STL, Obj, drc, gltf, glb.



Bara några mindre ändringar API.

### Lagt till ny fastighet i klass `com.aspose.threed.GltfSaveOptions`:

{{< highlight "java" >}}

    /**
     * Use external draco encoder to accelerate the draco compression speed.
     */
    public String getExternalDracoEncoder();
    
    /**
     * Use external draco encoder to accelerate the draco compression speed.
     * @param value New value
     */
    public void setExternalDracoEncoder(String value);


{{< /highlight >}}


Aspose.3D för java 21.4 har två gånger prestanda förbättring för Draco än gamla versioner, men den Google officiella genomförande som skrevs i C++ är fortfarande snabbare, så vi gör det möjligt för användaren att använda extern Draco kodare för bättre prestanda.


Provkod för att använda extern officiell kodare för att accelerera den komprimerade GLB generationen:

{{< highlight "java" >}}

        var mesh = new Sphere();
        var scene = new Scene(mesh);
        var opt = new GltfSaveOptions(FileFormat.GLTF2__BINARY);
        opt.setExternalDracoEncoder("D:\\Github\\draco\\sln\\Release\\draco_encoder.exe");
        opt.setDracoCompression(true);
        scene.save("test.glb", opt);

{{< /highlight >}}


{{% alert color="primary" %}} 
OBS: Denna egenskap kommer att markeras som föråldrad när vi förbättrat vår draco-kodning/avkodning prestanda till officiell implementering.
{{% /alert %}}

