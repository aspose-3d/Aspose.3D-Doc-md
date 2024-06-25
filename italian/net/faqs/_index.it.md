---
title: FAQs
type: docs
weight: 190
url: /it/net/faqs/
description: Domande frequenti su Aspose.3D per. Rete.
---
####  **D: Come animare FBX o altre proprietà speciali del formato 3D che non sono state definite in Aspose.3D?**
* A **: creare una proprietà dinamica sull'oggetto di destinazione ed eseguire l'animazione di proprietà sulla proprietà dinamica, poiché la proprietà dipende dal formato di file concreto, Aspose.3D non può garantire che l'animazione possa funzionare quando si salva la scena in un tipo di formato diverso.
####  **D: Perché l'animazione sul nodo radice della scena non funziona quando viene serializzata su un file FBX?**
* A **: Il formato FBX non consente di accedere alle proprietà del nodo radice, quindi l'animazione non funzionerà.
####  **D: Perché ho modificato le informazioni sulla scena e ho provato a importare il file FBX generato su 3ds max, queste informazioni sono andate tutte perse?**
* A **: 3Ds MAX o altri software possono importare solo file FBX, ma non aprire il file FBX, ciò significa che ti consente di importare più FBX all'interno di una scena, se le informazioni sulla risorsa possono essere applicate alla scena corrente, quindi le informazioni sulla scena originale potrebbero essere sovrascritte dall'importazione, Quindi questa è la politica di progettazione di 3Ds MAX per non importare le informazioni sugli asset della scena.


####  **D: Un nodo è costituito da più mesh (per il vetro, il telaio, ecc.). Tutte queste mesh si trovano nell'elenco delle entità del nodo. Come aggiungere un materiale a tutti quei nodi (il materiale è solo il colore)?**
* A **: La soluzione migliore dovrebbe creare sub-nodi per ogni mesh e assegnare materiale diverso a ciascun sotto nodo.