---
title: Cast e Ricevi Ombre su 3D Geometrie
type: docs
weight: 10
url: /it/net/cast-and-receive-shadows-on-3d-geometries/
description: In generale, alcuni formati di file 3D possono memorizzare le impostazioni relative alle ombre in geometria come FBX. Utilizzando Aspose.3D for .NET, gli sviluppatori possono eseguire il rendering di un'immagine mappando le ombre dal punto di vista di una sorgente luminosa. La qualità dell'immagine dipende dalla sorgente luminosa, dall'angolo di elevazione e dalla distanza tra la fotocamera e gli oggetti geometrici.
---
{{% alert color="primary" %}}

In generale, alcuni formati di file 3D possono memorizzare le impostazioni relative alle ombre in geometria come FBX. Utilizzo[Aspose.3D for .NET](https://products.aspose.com/3d/net/), Gli sviluppatori possono rendere un'immagine mappando le ombre dal punto di vista di una sorgente di luce. La qualità dell'immagine dipende dalla sorgente luminosa, dall'angolo di elevazione e dalla distanza tra la fotocamera e gli oggetti geometrici.

{{% /alert %}}
## **Trasmetti e ricevi l'ombra**
Per impostazione predefinita, tutti gli oggetti nella scena proiettano ombre da una sorgente luminosa. Gli sviluppatori possono anche ricevere ombre su base per oggetto nella superficie dell'oggetto. Questo esempio di codice rivela come impostare la posizione della luce e degli oggetti della fotocamera. Crea anche un piano e posiziona tre oggetti con diversi colori e impostazioni dell'ombra.

Tutte le geometrie hanno `CastShadows = true` e `ReceiveShadows=true`, le ombre della scatola rossa e del toro gettate sull'aereo, la scatola rossa non riceverà ombre e la scatola blu non proietterà ombre.
### **Campione di programmazione**
Questo esempio di codice proietta e riceve ombre su geometrie 3D.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Rendering-CastAndReceiveShadow-CastAndReceiveShadow.cs" >}}


**Risultato di rendering**

![Todo: immagine_Alt_Testo](cast-and-receive-shadows-on-3d-geometries_1.png)
