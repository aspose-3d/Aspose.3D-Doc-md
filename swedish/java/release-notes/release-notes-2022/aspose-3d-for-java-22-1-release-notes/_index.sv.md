---
title: Aspose.3D for Java 22,1 Utgivning
type: docs
weight: 12
url: /sv/java/aspose-3d-for-java-22-1-release-notes/
---
{{% alert color="primary" %}}

Denna sida innehåller release anteckningar för Aspose.3D for Java 22.1.

{{% /alert %}}
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|THREEDNET-1017 |Återställde stödet av netstandard2.0|Uppgifter|
|THREEDNET-1016 |Misslyckades öppna usdz-filer för att konvertera till glb|Felrättning|
|THREEDNET-1018 |Udda FBX fråga som orsakar Mesh att försvinna.|Felrättning|
|THREEDNET-1020 |Lägg till primitiva enheter för kodning i USD exportör|Ny funktion|
|THREEDNET-1021 |Lägg till primitiva enheter som avkodar stöd i USD exportör|Ny funktion|
|THREEDNET-1023 |Stränghantering var felaktig i USD importör/exportör|Felrättning|
|THREEDNET-1022 |USD fil med anpassadData kan inte öppnas|Felrättning|
|THREEDNET-1040 |Flera objekt med manuellt tilldelade objekt- id kan orsaka export till FBX misslyckades|Felrättning|


## API ändringar ##


I 22.1 har vi fixat några fel i FBX och USD, och lagt till primitiv export/export till USD.

USD stöder bara några få primitiver som Sfär, Cube, Cylinder, vi exporterar andra primitiver genom USD:s customData, sedan USD scener konverterade från CAD filer som RVM kan ha mycket mindre filstorlek.

Och i 22.1 webben renderare kan stödja USDZ filen direkt utan att konvertera till A3DW format nu.


### Lagt till klass Aspose.ThreeD.Formats.UsdSaveOptions.

UsdSaveOptions kan du ange hur du behandlar de primitiva under exporten, konvertera den till mesh för bästa kompatibilitet eller spara dem som parameteriserade geometrier för minsta filstorlek, vår webben renderare stöder de parametriserade geometrier som exporteras av Aspose.3D USDZ exportör, det är ett bäst alternativ för dig att presentera 3D innehåll med hjälp av vår web renderare.



{{< highlight "java" >}}

    var scene = new Scene();
    scene.getRootNode().createChildNode(new Cylinder());
    var opt = new UsdSaveOptions(FileFormat.USDZ);
    //default value is true for back compatibility, set it to false so we can generate smaller usdz file.
    opt.setPrimitiveToMesh(false);
    scene.save("test.usdz", opt);

{{< /highlight >}}
