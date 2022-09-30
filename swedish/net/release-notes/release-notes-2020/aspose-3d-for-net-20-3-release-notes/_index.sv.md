---
title: Aspose.3D for .NET 20,3 Utgivning
type: docs
weight: 50
url: /sv/net/aspose-3d-for-net-20-3-release-notes/
---
{{% alert color="primary" %}} 

Denna sida innehåller release anteckningar för Aspose.3D for .NET 20.3.

{{% /alert %}} 
## **Förbättringar och förändringar**

|**Nyckel**|**Sammanfattning**|**Kategori**|
|:- |:- |:- |
|THREEDNET-640 |` `Text renderingsstöd i webben renderare.|` `Förbättring|
|THREEDNET-637 |` `Ruler rendera i webben renderare.|` `Förbättring|
|THREEDNET-633 |` `SetProperty med noll värdeemission|` `Bug|
|THREEDNET-635 |` `Några exempel misslyckades i . Nettkärna 3.1 läge.|` `Bug|
|THREEDNET-634 |` `Projekt med .NET 3.1 kärnkast Undantag|` `Bug|
|THREEDNET-641 |` ` Undantag vid lastning 3D|` `Bug|
## **Offentlig API och bakåtkompatibla förändringar**
### **Nya medlemmar**
- Lagt till nya medlemmar i klass**Aspose.ThreeD. Format.HTML5SparaOptioner**



{{< highlight "java" >}}

 Scene s = new Scene("test.fbx");

s.Save("output.html", new HTML5SaveOptions() { ShowRulers = true });

{{< /highlight >}}
### **Föråldrade medlemmar borttagen**
- Följande markerades som föråldrade i**19.12.9**Och har tagits bort ifrån**Aspose.ThreeD.Animation Kanal**Nu.
- Offentlig tomrum AddCurve(Aspose.ThreeD.Animation.KeyframeSequence kurva)
- Offentliga system.Samling.Generic.IList.<Aspose.ThreeD.Animation.KeyframeSequence>Kurvor{ get;}
- Följande markerades som föråldrade i**19.12.9**Och har tagits bort ifrån**Aspose.ThreeD.AnimationNode.**Nu.
- Public Aspose.ThreeD.Animation.BindPoint FindCurveMapping(strängnamn)
- Offentlig Aspose.ThreeD. Animation. BindPoint GetCurve Mapping(Aspose.ThreeD. A3DObject mål, sträng propName, bool skapa)
- Offentlig Aspose.ThreeD. Animation. NyckelframeSequence GetCurve(Aspose.ThreeD. A3DObjekt mål, sträng propName, strängkanalNamn, bool create)
- Offentlig Aspose.ThreeD. Animation. NyckelframeSequence GetCurve(Aspose.ThreeD. A3DObject mål, sträng propName, bool skapa)
- Offentlig Aspose.ThreeD. Animation. BindPoint CreateCurveMapping(Aspose.ThreeD. A3DObject obj, sträng propName)
- Offentliga system.Samling.Generic.IList.<Aspose.ThreeD.Animation.BindPoint>CurveMappings { get;}
- Följande markerades som föråldrade i**19.12.9**Och har tagits bort ifrån**Aspose.ThreeD.Animation.BindPoint.**Nu.
- Public Aspose.ThreeD.Animation.nyckelframeSequence GetCurve(streng kanalNamn)
- Offentliga system.Samling.Generic.IList.<Aspose.ThreeD.Animation.KeyframeSequence>GetCurves( strängkanalnamn)
- Public Aspose.ThreeD.Animation.nyckelframeSequence CreateCurve(sträng kurveName)
- Public void BindCurve(streng kanalNamn, Aspose.ThreeD.Animering.KeyframeSequence kurva)
- Följande ledamöter markerades som föråldrade i**19.12.9**Och har tagits bort ifrån**Aspose.ThreeD.Animation.KeyFrameSequens**Nu.
- Public Aspose.ThreeD.Animation.BindPoint CurveMapping { get;}
- Följande ledamöter markerades som föråldrade i**19.12.9**Och har tagits bort ifrån**Aspose.ThreeD.Egang**Nu.
- Offentlig Aspose.ThreeD. Animation. BindPoint GetCurve Mapping(Aspose.ThreeD. Animation. AnimationNode anim, bool create)
- Offentlig Aspose.ThreeD. Animation. NyckelframeSequence GetCurve(Aspose.ThreeD. Animation. AnimationNode anim, bool create)
- Offentlig tomrum SetFlags(Aspose.ThreeD.PropertyFlags f, bool set)
- Följande klass markerad som föråldrad**19.12.9**Och har tagits bort nu.
  - **Aspose.ThreeD Enheter.ManualEntity**

