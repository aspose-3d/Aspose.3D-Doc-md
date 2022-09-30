---
title: Aspose.3D for Java 20,3 Utgivning
type: docs
weight: 50
url: /sv/java/aspose-3d-for-java-20-3-release-notes/
---
{{% alert color="primary" %}} 

Denna sida innehåller release anteckningar för Aspose.3D for Java 20.3.

{{% /alert %}} 
## **Förbättringar och förändringar**

|` `**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|THREEDNET-640 |` `Text renderingsstöd i webben renderare.|` `Förbättring|
|THREEDNET-637 |` `Ruler rendera i webben renderare.|` `Förbättring|
|THREEDNET-633 |` `SetProperty med noll värdeemission|` `Bug|
|THREEDNET-635 |` `Några exempel misslyckades i . Nettkärna 3.1 läge.|` `Bug|
|THREEDNET-634 |` `Projekt med .NET 3.1 kärnkast Undantag|` `Bug|
|THREEDNET-641 |` ` Undantag vid lastning 3D|` `Bug|
## **Offentlig API och bakåtkompatibla förändringar**
### **Nya medlemmar**
- Lagt till nya medlemmar i klass**Com.aspose. Threed.HTML5SaveOptionComment**

{{< highlight "java" >}}

 Scene s = new Scene("test.fbx");

HTML5SaveOptions opt = new HTML5SaveOptions();

HTML5SaveOptions.setShowRulers(true);

s.save("output.html", opt);

{{< /highlight >}}
### **Föråldrade medlemmar borttagen**
- Följande markerades som föråldrade i**19.12.9**Och har tagits bort ifrån**Com.aspose. Threed.Animationskanal**Nu.
- Offentlig tomrum com. Förmodligen. Tre. AnimationChannel. AddCurve( s. Förmodligen. Tre. NyckelframeSequence;
- Public java.util.List.<com.aspose.threed.KeyframeSequence>Com.aspose.treed.AnimationChannel.getCurves ();
- Följande markerades som föråldrade i**19.12.9**Och har tagits bort ifrån**Com.aspose. Threed.AnimationNodeName**Nu.
- Offentlig kommunikation. Förmodligen. Tre. NyckelframeSequence com. Förmodligen. Tre. AnimationNode. (f) Förmodligen. Tre. A3DObjekt, java. Lang. String, java. Lang. Sträng, boole.
- Offentlig kommunikation. Förmodligen. Tre. NyckelframeSequence com. Förmodligen. Tre. AnimationNode. (f) Förmodligen. Tre. A3DObjekt, java. Lang. Sträng, boole.
- Offentlig kommunikation. Förmodligen. Tre. -BindPoint com. Förmodligen. Tre. AnimationNode.createCurveMapping(com. Förmodligen. Tre. A3DObjekt, java. Lang. Sträng.
- Public java.util.List.<com.aspose.threed.BindPoint>Com.aspose.3reed.AnimationNode.getCurveMappings ();
- Offentlig kommunikation. Förmodligen. Tre. -BindPoint com. Förmodligen. Tre. AnimationNode. FindCurveMapping( java. Lang. Sträng.
- Offentlig kommunikation. Förmodligen. Tre. -BindPoint com. Förmodligen. Tre. AnimationNode.getCurveMapping(com. Förmodligen. Tre. A3DObjekt, java. Lang. Sträng, boole.
- Följande markerades som föråldrade i**19.12.9**Och har tagits bort ifrån**Com.aspose.3.BindPoint.**Nu.
- Offentlig kommunikation. Förmodligen. Tre. NyckelframeSequence com. Förmodligen. Tre. -BindPoint. (Java. Lang. Sträng.
- Public java.util.List.<com.aspose.threed.KeyframeSequence>Com.aspose.treed.BindPoint.getCurves(java.lang.String)
- Offentlig tomrum com. Förmodligen. Tre. -BindPoint. BinCurve (java). Lang. String, com. Förmodligen. Tre. NyckelframeSequence;
- Offentlig kommunikation. Förmodligen. Tre. NyckelframeSequence com. Förmodligen. Tre. -BindPoint. CreateCurve (java. Lang. Sträng.
- Följande ledamöter markerades som föråldrade i**19.12.9**Och har tagits bort ifrån**Com.aspose.**Nu.
- Offentlig kommunikation. Förmodligen. Tre. -BindPoint com. Förmodligen. Tre. NyckelframeSequence.getCurveMapping ();
- Följande ledamöter markerades som föråldrade i**19.12.9**Och har tagits bort ifrån**Com.aspose.**Nu.
- Offentlig kommunikation. Förmodligen. Tre. -BindPoint com. Förmodligen. Tre. Egendom.getCurveMapping(com. Förmodligen. Tre. AnimationNode anim,boolean create;
- Offentlig kommunikation. Förmodligen. Tre. NyckelframeSequence com. Förmodligen. Tre. Egendom. (f) Förmodligen. Tre. AnimationNode anim,boolean create;
- Följande klass markerad som föråldrad**19.12.9**Och har tagits bort nu.
  - **Com.aspose. Threed.ManualEntity**
