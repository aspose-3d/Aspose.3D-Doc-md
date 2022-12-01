---
title: Aspose.3D for Java 21.5 Note di rilascio
type: docs
weight: 8
url: /it/java/aspose-3d-for-java-21-5-release-notes/
---
{{% alert color="primary" %}}

Questa pagina contiene le informazioni sulle note di rilascio per lo Aspose.3D for Java 21.5.

{{% /alert %}}
## **Miglioramenti e modifiche**
|**Chiave**|**Riassunto**|**Categoria**|
|:- |:- |:- |
|THREEDNET-878 |Disegna il bordo nero attorno ai poligoni|Nuova funzione|
|THREEDNET-879 |Convertire STL in GLB risultati in un attributo non valido: “/meshes/0/primitive/0/attributi/NORMAL _ 0”|Correzione di bug|
|THREEDNET-885 |Il renderer Aspose.3D si è bloccato a causa della grande rete caricata.|Correzione di bug|
|THREEDNET-884 |Convalida in file convertiti GLB.|Miglioramento|
|THREEDNET-882 |Il file GLB generato non viene eseguito il rendering in Babylon.js|Correzione di bug|
|THREEDNET-887 |Convertire l'immagine in jpg/png quando l'utente esporta glTF con risorse incorporate|Nuova funzione|

## API modifiche ##


### Aggiunto nuovo tipo di enum `com.aspose.threed.GltfEmbeddedImageFormat`: ###

{{< highlight "java" >}}
/**
 * How glTF exporter will embed the textures during the exporting.
 */
public enum GltfEmbeddedImageFormat
{    
    /**
     * Do not convert the image and keep it as it is.
     */
    NO_CHANGE,
    /**
     * All non-supported images formats will be converted to jpeg if possible.
     */
    JPEG,
    /**
     * All non-supported images formats will be converted to png if possible.
     */
    PNG;
}
{{< /highlight >}}

### Aggiunta nuova proprietà nel `com.aspose.threed.GltfSaveOptions`:

{{< highlight "java" >}}
    public GltfEmbeddedImageFormat getImageFormat();
    public void setImageFormat(GltfEmbeddedImageFormat value);
{{< /highlight >}}


Lo standard glTF supporta solo PNG/JPG come formato texture, questa opzione guiderà come Aspose.3D convertirà le immagini non standard nel formato supportato durante l'esportazione.

Il valore predefinito è GltfEmbeddedImageFormat.PNG, quindi la texture incorporata verrà convertita in png, di solito non è necessario modificarla manualmente.


# Aggiunta nuova proprietà nel `com.aspose.threed.GltfSaveOptions`:

{{< highlight "java" >}}
    public void setFallbackNormal(Vector3 value);
    public Vector3 getFallbackNormal();
{{< /highlight >}}

Quando l'esportatore GLTF2 rileva una normalità non valida dalla scena, questa verrà utilizzata al posto del suo valore originale per aggirare la convalida, questo accade se la scena è stata importata da un file esportato con dati errati.

Il valore predefinito è (0, 1, 0).

Se assegna questo valore con null, i dati normali errati verranno superati senza alcuna modifica.

