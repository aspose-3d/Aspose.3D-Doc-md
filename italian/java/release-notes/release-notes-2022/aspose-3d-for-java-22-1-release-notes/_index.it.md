---
title: Aspose.3D for Java Note di rilascio 22.1
type: docs
weight: 12
url: /it/java/aspose-3d-for-java-22-1-release-notes/
---
{{% alert color="primary" %}}

Questa pagina contiene le informazioni sulle note di rilascio per lo Aspose.3D for Java 22.1.

{{% /alert %}}
## **Miglioramenti e modifiche**

|**Chiave**|**Riassunto**|**Categoria**|
|:- |:- |:- |
|THREEDNET-1017 |Ripristinato il supporto di netstandard2.0|Attività|
|THREEDNET-1016 |Impossibile aprire i file usdz da convertire in glb|Correzione di bug|
|THREEDNET-1018 |Problema dispari FBX che causa la scomparsa di Mesh|Correzione di bug|
|THREEDNET-1020 |Aggiungi il supporto per la codifica di entità primitive nell'esportatore USD|Nuova funzionalità|
|THREEDNET-1021 |Aggiungi il supporto per la decodifica delle entità primitive nell'esportatore USD|Nuova funzionalità|
|THREEDNET-1023 |La manipolazione delle stringhe non era corretta nello USD importatore/esportatore|Correzione di bug|
|THREEDNET-1022 |Il file USD con customData non può essere aperto|Correzione di bug|
|THREEDNET-1040 |Più oggetti con ID oggetto assegnato manualmente possono causare l'esportazione in FBX non riuscita|Correzione di bug|


## API modifiche ##


Nel 22.1 abbiamo corretto alcuni bug negli FBX e USD e aggiunto l'esportazione/esportazione primitiva allo USD.

USD supporta solo alcune primitive come Sphere, Cube, Cylinder, esportiamo altre primitive tramite CustomData di USD, quindi USD scene convertite da file CAD come RVM possono avere file di dimensioni molto più piccole.

E in 22.1 il renderer web può supportare il file USDZ direttamente senza convertire in formato A3DW ora.


### Classe aggiunta Aspose.ThreeD. Formati. UsdSaveOptions

UsdSaveOptions consente di specificare come trattare le primitive durante l'esportazione, convertirlo in mesh per la migliore compatibilità o salvarli come geometrie parametrizzate per le dimensioni più piccole del file, il nostro renderer web supporta le geometrie parametrizzate esportate da Aspose.3D esportatore USDZ, è un'opzione migliore per presentare i contenuti 3D utilizzando il nostro renderer web.



{{< highlight "java" >}}

    var scene = new Scene();
    scene.getRootNode().createChildNode(new Cylinder());
    var opt = new UsdSaveOptions(FileFormat.USDZ);
    //default value is true for back compatibility, set it to false so we can generate smaller usdz file.
    opt.setPrimitiveToMesh(false);
    scene.save("test.usdz", opt);

{{< /highlight >}}
