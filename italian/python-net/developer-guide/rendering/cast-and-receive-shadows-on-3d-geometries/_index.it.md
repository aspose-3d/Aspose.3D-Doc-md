---
title: Lanciare e ricevere ombre su 3D geometrie
type: docs
weight: 10
url: /it/python-net/cast-and-receive-shadows-on-3d-geometries/
description: In generale, alcuni formati di file 3D possono memorizzare le impostazioni relative alle ombre in geometria come FBX. Utilizzando Aspose.3D for Python via .NET, gli sviluppatori possono eseguire il rendering di un'immagine mappando le ombre dal punto di vista di una sorgente luminosa. La qualità dell'immagine dipende dalla sorgente luminosa, dall'angolo di elevazione e dalla distanza tra la fotocamera e gli oggetti geometrici.
---
{{% alert color="primary" %}}

In generale, alcuni formati di file 3D possono memorizzare le impostazioni relative alle ombre in geometria come FBX. Utilizzando [Aspose.3D for Python via .NET](https://products.aspose.com/3d/python-net/), gli sviluppatori possono eseguire il rendering di un'immagine mappando le ombre dal punto di vista di una sorgente luminosa. La qualità dell'immagine dipende dalla sorgente luminosa, dall'angolo di elevazione e dalla distanza tra la fotocamera e gli oggetti geometrici.

{{% /alert %}}
##  **Trasmetti e ricevi l'ombra**
Per impostazione predefinita, tutti gli oggetti nella scena proiettano ombre da una sorgente luminosa. Gli sviluppatori possono anche ricevere ombre su base per oggetto nella superficie dell'oggetto. Questo esempio di codice rivela come impostare la posizione della luce e degli oggetti della fotocamera. Crea anche un piano e posiziona tre oggetti con diversi colori e impostazioni dell'ombra.

Tutte le geometrie hanno `cast_shadows = True` e `receive_shadows = True`, le ombre della scatola rossa e del toro gettate sull'aereo, la scatola rossa non riceverà ombre e la scatola blu non proietterà ombre.
###  **Campione di programmazione**
Questo esempio di codice proietta e riceve ombre su geometrie 3D.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Rendering-CastAndReceiveShadow-CastAndReceiveShadow.py" >}}


**Risultato di rendering**

! [Todo: image_alt_text](cast-and-receive-shadows-on-3d-geometries_1.png)
