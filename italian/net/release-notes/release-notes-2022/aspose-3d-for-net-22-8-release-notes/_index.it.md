---
title: Aspose.3D for .NET Note di rilascio 22.8
type: docs
weight: 5
url: /it/net/aspose-3d-for-net-22-8-release-notes/
description: Le note di rilascio dello Aspose.3D for .NET 22,8.
---
{{% alert color="primary" %}}

Questa pagina contiene le informazioni sulle note di rilascio per lo Aspose.3D for .NET 22.8.

{{% /alert %}}
## **Miglioramenti e modifiche**

|**Chiave**|**Riassunto**|**Categoria**|
|:- |:- |:- |
|THREEDNET-1175 |Risolvi i problemi relativi al file del pacchetto di rilascio.|Attività|
|THREEDNET-1183 |Risolvi la directory di installazione predefinita del pacchetto MSI|Attività|
|THREEDNET-1176 |Il nodo con traduzione geometrica non può essere gestito correttamente nell'esportatore USDZ.|Correzione di bug|
|THREEDNET-1179 |Aspose.3D 22.5: Eccezione quando si cerca di caricare il file Vrml|Correzione di bug|
|THREEDNET-1181 |Aspose.3D 22.5: Impossibile convertire USD a 3DS|Correzione di bug|
|THREEDNET-1184 |AccessViolationException su alcuni file GLTF.|Correzione di bug|
|THREEDNET-1186 |Aggiungi supporto operatore xform personalizzato in USD/USDZ importatore|Miglioramento|
|THREEDNET-1187 |Il materiale non funziona nel file generato USD/USDZ.|Correzione di bug|
|THREEDNET-1188 |Gli attributi del materiale non vengono esportati quando nessuna trama è allegata|Correzione di bug|
|THREEDNET-1189 |I modelli convertiti da FBX a USDZ sono tutti neri|Correzione di bug|
|THREEDNET-1190 |Aggiungere il convertitore materiale per l'esportatore USD/USDZ|Miglioramento|
|THREEDNET-1191 |Il visualizzatore lancia un'eccezione quando due primitive sono collegate a un nodo.|Correzione di bug|
|THREEDNET-1192 |InitializationException durante l'inizializzazione della finestra di rendering|Correzione di bug|
|THREEDNET-1194 |FBX Eccezioni: la chiave data "OSL" non era presente nel dizionario|Correzione di bug|
|THREEDNET-1195 |GLTF Eccezione: la stringa di input non era in un formato corretto.|Correzione di bug|
|THREEDNET-1196 |GLTF Eccezione: Aspose.ThreeD.Utilities.Unexpected TokenException: ''Unexpected token 'NaN''|Correzione di bug|
|THREEDNET-1197 |GLTF Eccezione: System.ArgumentException: "È già stato aggiunto un elemento con la stessa chiave. Chiave: pcInfoFieldName'|Correzione di bug|
|THREEDNET-1198 |FBX Eccezione: Aspose.ThreeD. Eccezione: "MultiLayer di proprietà illegale durante la deserializzazione di Aspose.ThreeD.Entities.NullNode Armate"|Correzione di bug|
|THREEDNET-1199 |FBX Eccezione: System.InvalidCastException: "Impossibile lanciare l'oggetto del tipo" System.Single[] "per digitare" Aspose.ThreeD.Utilities.DoubleList "."|Correzione di bug|
|THREEDNET-1200 |USD Eccezione: il tipo di dati UsdTimeCode non è supportato|Correzione di bug|
|THREEDNET-1201 |USD Eccezione: UsdQuatf non è implementato.|Correzione di bug|
|THREEDNET-1202 |USD Eccezione: UsdVec3h non è supportato|Correzione di bug|
|THREEDNET-1203 |USD Eccezione: il tipo di dizionario Inlinlined non è implementato|Correzione di bug|
|THREEDNET-1204 |USD Eccezione: Vec2d non è supportato|Correzione di bug|
|THREEDNET-1205 |USD Eccezione: non è possibile aprire questo file|Correzione di bug|
|THREEDNET-1206 |USD Eccezione: specificatore duplicato per SdfPath|Correzione di bug|
|THREEDNET-1207 |USD Eccezione: xformOp:orient non è supportato.|Correzione di bug|
|THREEDNET-1208 |L'encoder draco esterno non funziona.|Correzione di bug|
|THREEDNET-1209 |DAE Risparmia allo USD Eccezione: System.IndexOutOfRangeException: "L'indice era al di fuori dei limiti dell'array".|Correzione di bug|


Questa versione ha risolto un sacco di bug e non ha importanti modifiche API.

## API modifiche ##


### Aggiunta nuova proprietà MaterialConverter in classe `Aspose.ThreeD.Formats.UsdSaveOptions`:

{{< highlight "csharp" >}}
        /// <summary>
        /// Custom converter to convert the geometry's material to PBR material
        /// If this is unassigned, USD exporter will automatically convert the standard material to PBR material.
        /// Default value is null
        /// </summary>
        public Aspose.ThreeD.Formats.MaterialConverter MaterialConverter{ get;set; }
{{< /highlight >}}



Aspose.3D ha un'implementazione integrata per convertire materiale non PBR in materiale PBR per formati glTF/USD/USD, ma forniamo anche implementazione personalizzata per effettuare la conversione.



### Proprietà aggiornate per supportare le nuove definizioni dei materiali FBX:

Vecchie definizioni:

{{< highlight "csharp" >}}
        public Aspose.ThreeD.Shading.ShadingLanguage ShaderLanguage{ get;set;}
        public Aspose.ThreeD.Shading.RenderingAPI RenderAPI{ get;set;}
{{< /highlight >}}

Nuove definizioni:

{{< highlight "csharp" >}}
        public string ShaderLanguage{ get;set;}
        public string RenderAPI{ get;set;}
{{< /highlight >}}
		
		




