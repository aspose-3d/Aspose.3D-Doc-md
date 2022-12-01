---
title: Aspose.3D for Java 22,8 Utgivning
type: docs
weight: 5
url: /sv/java/aspose-3d-for-java-22-8-release-notes/
description: Publiceringsnoterna av Aspose.3D for Java 22.8.
---
{{% alert color="primary" %}}

Denna sida innehåller release anteckningar för Aspose.3D for Java 22.8.

{{% /alert %}}
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|THREEDNET-1175 |Fix release paket problem.|Uppgifter|
|THREEDNET-1183 |Fixa standard installationskatalog för MSI-paket|Uppgifter|
|THREEDNET-1176 |Nod med geometri översättning kan inte hanteras korrekt i USDZ exportör.|Felrättning|
|THREEDNET-1179 |Aspose.3D 22.5: Undantag vid försök att ladda Vrml-filen|Felrättning|
|THREEDNET-1181 |Aspose.3D 22.5: Kan inte konvertera USD till 3DS|Felrättning|
|THREEDNET-1184 |AccessViolationException på några GLTF filer.|Felrättning|
|THREEDNET-1186 |Lägg till anpassad xform operator support i 0761481/USDZ importör|Förbättring|
|THREEDNET-1187 |Material fungerar inte i genererad USD/USDZ fil.|Felrättning|
|THREEDNET-1188 |Materialattribut exporteras inte när ingen textur ansluts|Felrättning|
|THREEDNET-1189 |Modeller som omvandlats från FBX till USDZ är alla svart|Felrättning|
|THREEDNET-1190 |Lägg till materialConverter för USD/USDZ exportör|Förbättring|
|THREEDNET-1191 |Visare kastar undantag när två primitiver fästs vid en nod.|Felrättning|
|THREEDNET-1192 |InitialiseringException under initiering av renderingsfönstret|Felrättning|
|THREEDNET-1194 |FBX Undantag: Den givna nyckeln "OSL" fanns inte i ordboken|Felrättning|
|THREEDNET-1195 |GLTF Undantag: Inmatningssträngen var inte i rätt format.|Felrättning|
|THREEDNET-1196 |GLTF Undantag: Aspose.ThreeD. -Det är det. UnexpectedTokenException: 'Unväntad token 'NaN''|Felrättning|
|THREEDNET-1197 |GLTF Undantag: System.ArgumentUndantag: "En artikel med samma nyckel har redan lagts till. Nyckel: pcInfoFieldName'|Felrättning|
|THREEDNET-1198 |FBX Undantag: Aspose.ThreeD. ImportException: 'Olegal egendom MultiLayer medan deserialisering Aspose.ThreeD. Enheter. "NullNode Armature"|Felrättning|
|THREEDNET-1199 |FBX Undantag: System. FelaktigCastException: 'Kan inte kasta objekt av typ' System. Ensam[]' för att skriva 'Aspose.ThreeD. -Det är det. Dubbellista."|Felrättning|
|THREEDNET-1200 |USD Undantag: Datatyp UsdTimeCode stöds inte|Felrättning|
|THREEDNET-1201 |USD Undantag: UsdQuatf är inte implementerat.|Felrättning|
|THREEDNET-1202 |USD Undantag: UsdVec3h stöds inte|Felrättning|
|THREEDNET-1203 |USD Undantag: Inlined ordbok är inte implementerad|Felrättning|
|THREEDNET-1204 |USD Undantag: Vec2d stöds inte|Felrättning|
|THREEDNET-1205 |USD Undantag: Kan inte öppna den här filen|Felrättning|
|THREEDNET-1206 |USD Undantag: Duplicerad specifikation för SdfPath.|Felrättning|
|THREEDNET-1207 |USD Undantag: xformOp:orient stöds inte.|Felrättning|
|THREEDNET-1208 |Den externa draco- kodaren fungerar inte.|Felrättning|
|THREEDNET-1209 |DAE Spara till USD Undantag: System. IndexOutOfRangeException: 'Index låg utanför matrisens gränser."|Felrättning|


Denna version fixade en massa fel och har inte större API ändringar.

## API ändringar ##


### Lagt till nya metoder i klass `com.aspose.threed.UsdSaveOptions`:

{{< highlight "java" >}}
    /**
     * Custom converter to convert the geometry's material to PBR material
     * If this is unassigned, USD exporter will automatically convert the standard material to PBR material.
     * Default value is null
     */
    public MaterialConverter getMaterialConverter();
    /**
     * Custom converter to convert the geometry's material to PBR material
     * If this is unassigned, USD exporter will automatically convert the standard material to PBR material.
     * Default value is null
     * @param value New value
     */
    public void setMaterialConverter(MaterialConverter value);
{{< /highlight >}}



Aspose.3D har en inbyggd implementering för att konvertera icke-baserade material till PBR material för glTF/USD/077 6133481 format, men vi tillhandahåller även anpassad genomförande för att göra konverteringen.



### Uppdaterade egenskaper för att stödja nya FBX materialdefinitioner:

Gamla definitioner:

{{< highlight "csharp" >}}
    /**
     * Gets the shader language used by this technique.
     */
    public ShadingLanguage getShaderLanguage();
    
    /**
     * Sets the shader language used by this technique.
     * @param value New value
     */
    public void setShaderLanguage(ShadingLanguage value);
    /**
     * Gets the rendering API used by this technique
     */
    public RenderingAPI getRenderAPI();
    
    /**
     * Sets the rendering API used by this technique
     * @param value New value
     */
    public void setRenderAPI(RenderingAPI value);
{{< /highlight >}}

Nya definitioner:

{{< highlight "java" >}}
    /**
     * Gets the shader language used by this technique.
     */
    public String getShaderLanguage();
    
    /**
     * Sets the shader language used by this technique.
     * @param value New value
     */
    public void setShaderLanguage(String value);
    /**
     * Gets the rendering API used by this technique
     */
    public String getRenderAPI();
    
    /**
     * Sets the rendering API used by this technique
     * @param value New value
     */
    public void setRenderAPI(String value);
{{< /highlight >}}
		
		




