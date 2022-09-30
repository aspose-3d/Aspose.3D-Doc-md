---
title: Aspose.3D for .NET 20.3 Note di rilascio
type: docs
weight: 50
url: /it/net/aspose-3d-for-net-20-3-release-notes/
---
{{% alert color="primary" %}} 

Questa pagina contiene le informazioni sulle note di rilascio per lo Aspose.3D for .NET 20.3.

{{% /alert %}} 
## **Miglioramenti e modifiche**

|**Chiave**|**Riassunto**|**Categoria**|
|:- |:- |:- |
|THREEDNET-640 |` ` Supporto per il rendering del testo nel renderer web.|` ` Potenziamento|
|THREEDNET-637 |` `Ruler rendering in renderer web.|` ` Potenziamento|
|THREEDNET-633 |` ` proprietà Setcon problema di valore nullo|` `Bug|
|THREEDNET-635 |` ` Alcuni esempi hanno fallito. Modalità net core 3.1.|` `Bug|
|THREEDNET-634 |` ` Progetti con .NET 3,1 core getta Eccezione|` `Bug|
|THREEDNET-641 |` ` Eccezione sul caricamento del file 3D|` `Bug|
## **Pubblico API e modifiche incompatibili arretrate**
### **Nuovi membri aggiunti**
- Aggiunti nuovi membri in classe**Aspose.ThreeD. Formati. HTML5SaveOptions**



{{< highlight "java" >}}

 Scene s = new Scene("test.fbx");

s.Save("output.html", new HTML5SaveOptions() { ShowRulers = true });

{{< /highlight >}}
### **Membri obsoleti rimossi**
- Di seguito sono stati contrassegnati come obsoleti in**19.12**E sono stati rimossi da**Aspose.ThreeD. Animazione. AnimationChannel**Ora
-Void pubblico AddCurve(Aspose.ThreeD. Animazione. Curva KeyframeSequence)
-Sistema pubblico. Collezioni. Generic. Ilist<Aspose.ThreeD.Animation.KeyframeSequence>Curve {get;}
- I seguenti sono stati contrassegnati come obsoleti in**19.12**E sono stati rimossi da**Aspose.ThreeD. Animazione. Nodo di animazione**Ora
-Pubblico Aspose.ThreeD. Animazione. BindPoint FindCurveMapping (nome della stringa)
-Pubblico Aspose.ThreeD. Animazione. BindPoint GetCurveMapping(Aspose.ThreeD.A3DObject target, stringa propName, bool creare)
-Pubblico Aspose.ThreeD. Animazione. KeyframeSequence GetCurve(Aspose.ThreeD.A3DObject target, stringa propName, stringa channelName, bool creare)
-Pubblico Aspose.ThreeD. Animazione. KeyframeSequence GetCurve(Aspose.ThreeD.A3DObject target, stringa propName, bool creare)
-Pubblico Aspose.ThreeD. Animazione. BindPoint CreateCurveMapping(Aspose.ThreeD.A3DObject obj, stringa propName)
-Sistema pubblico. Collezioni. Generic. Ilist<Aspose.ThreeD.Animation.BindPoint>CurveMappings{ get;}
- I seguenti sono stati contrassegnati come obsoleti in**19.12**E sono stati rimossi da**Aspose.ThreeD. Animazione. BindPoint**Ora
-Pubblico Aspose.ThreeD. Animazione. KeyframeSequence GetCurve (stringa channelName)
-Sistema pubblico. Collezioni. Generic. Ilist<Aspose.ThreeD.Animation.KeyframeSequence>GetCurves (stringa channelName)
-Pubblico Aspose.ThreeD. Animazione. KeyframeSequence CreateCurve (stringa curveName)
-Void pubblico BindCurve (stringa channelName, Aspose.ThreeD. Animazione. Curva KeyframeSequence)
- I seguenti membri sono stati contrassegnati come obsoleti in**19.12**E sono stati rimossi da**Aspose.ThreeD. Animazione. KeyFrameSequence**Ora
-Pubblico Aspose.ThreeD. Animazione. BindPoint CurveMapping{ get;}
- I seguenti membri sono stati contrassegnati come obsoleti in**19.12**E sono stati rimossi da**Aspose.ThreeD. Immobile**Ora
-Pubblico Aspose.ThreeD. Animazione. BindPoint GetCurveMapping(Aspose.ThreeD. Animazione. AnimationNode anim, bool creare)
-Pubblico Aspose.ThreeD. Animazione. KeyframeSequence GetCurve(Aspose.ThreeD. Animazione. AnimationNode anim, bool creare)
-Pubblico void SetFlags(Aspose.ThreeD.PropertyFlags f, bool set)
- Classe seguente contrassegnata come obsoleta in**19.12**Ed è stato rimosso ora
  - **Aspose.ThreeD.Entità. ManualEntità**

