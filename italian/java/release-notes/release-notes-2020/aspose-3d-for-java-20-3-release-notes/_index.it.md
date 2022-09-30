---
title: Aspose.3D for Java 20.3 Note di rilascio
type: docs
weight: 50
url: /it/java/aspose-3d-for-java-20-3-release-notes/
---
{{% alert color="primary" %}} 

Questa pagina contiene le informazioni sulle note di rilascio per lo Aspose.3D for Java 20.3.

{{% /alert %}} 
## **Miglioramenti e modifiche**

|` `**Chiave**|**Riassunto**|**Categoria**|
|:- |:- |:- |
|THREEDNET-640 |` ` Supporto per il rendering del testo nel renderer web.|` ` Potenziamento|
|THREEDNET-637 |` `Ruler rendering in renderer web.|` ` Potenziamento|
|THREEDNET-633 |` ` proprietà Setcon problema di valore nullo|` `Bug|
|THREEDNET-635 |` ` Alcuni esempi hanno fallito. Modalità net core 3.1.|` `Bug|
|THREEDNET-634 |` ` Progetti con .NET 3,1 core getta Eccezione|` `Bug|
|THREEDNET-641 |` ` Eccezione sul caricamento del file 3D|` `Bug|
## **Pubblico API e modifiche incompatibili arretrate**
### **Nuovi membri aggiunti**
- Aggiunti nuovi membri in classe**Com. aspose.threed.HTML5SaveOptions**

{{< highlight "java" >}}

 Scene s = new Scene("test.fbx");

HTML5SaveOptions opt = new HTML5SaveOptions();

HTML5SaveOptions.setShowRulers(true);

s.save("output.html", opt);

{{< /highlight >}}
### **Membri obsoleti rimossi**
- Di seguito sono stati contrassegnati come obsoleti in**19.12**E sono stati rimossi da**Com. aspose.threed.AnimationChannel**Ora
-Public void com.aspose.threed.AnimationChannel.addCurve(com.aspose.threed.KeyframeSequence);
-Elenco java.util. pubblico<com.aspose.threed.KeyframeSequence>Com. aspose.threed.AnimationChannel.getCurves();
- I seguenti sono stati contrassegnati come obsoleti in**19.12**E sono stati rimossi da**Com. aspose.threed. Nodo di animazione**Ora
-Public com.aspose.threed.KeyframeSequence com.aspose.threed.AnimationNode.getCurve(com.aspose.threed.A3DObject,java.lang.String, booleano);
-Public com.aspose.threed.KeyframeSequence com.aspose.threed.AnimationNode.getCurve(com.aspose.threed.A3DObject,java.lang.String, booleano);
-Public com.aspose.threed.BindPoint com.aspose.threed.AnimationNode.createCurveMapping(com.aspose.threed.A3DObject,java.lang.String);
-Elenco java.util. pubblico<com.aspose.threed.BindPoint>Com. aspose.threed.AnimationNode.getCurveMappings();
-Public com.aspose.threed.BindPoint com.aspose.threed.AnimationNode.findCurveMapping(java.lang.String);
-Public com.aspose.threed.BindPoint com.aspose.threed.AnimationNode.getCurveMapping(com.aspose.threed.A3DObject,java.lang.String, booleano);
- I seguenti sono stati contrassegnati come obsoleti in**19.12**E sono stati rimossi da**Com. aspose.threed.BindPoint**Ora
-Public com.aspose.threed.KeyframeSequence com.aspose.threed.BindPoint.getCurve(java.lang.String);
-Elenco java.util. pubblico<com.aspose.threed.KeyframeSequence>Com. aspose.threed.BindPoint.getCurve (java.lang. Stringa);
-Public void com.aspose.threed.BindPoint.bindCurve(java.lang.String,com.aspose.threed.KeyframeSequence);
-Public com.aspose.threed.KeyframeSequence com.aspose.threed.BindPoint.createCurve(java.lang.String);
- I seguenti membri sono stati contrassegnati come obsoleti in**19.12**E sono stati rimossi da**Com. aspose.threed.KeyFrameSequence**Ora
-Public com.aspose.threed.BindPoint com.aspose.threed.KeyframeSequence.getCurveMapping();
- I seguenti membri sono stati contrassegnati come obsoleti in**19.12**E sono stati rimossi da**Com. aspose.threed. Proprietà**Ora
-Public com.aspose.threed.BindPoint com.aspose.threed.Property.getCurveMapping(com.aspose.threed.AnimationNode anim,boolean create);
-Public com.aspose.threed.KeyframeSequence com.aspose.threed.Property.getCurve(com.aspose.threed.AnimationNode anim,boolean crean);
- Classe seguente contrassegnata come obsoleta in**19.12**Ed è stato rimosso ora
  - **Com. aspose.threed. ManualEntità**
