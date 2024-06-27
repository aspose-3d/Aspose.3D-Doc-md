---
title: Crea e leggi una scena 3D esistente
type: docs
weight: 10
url: /it/net/create-and-read-an-existing-3d-scene/
description: Aspose.3D API supporta la creazione delle nuove scene 3D da zero e quindi il salvataggio in qualsiasi formato di file supportato. Gli sviluppatori possono anche caricare una scena 3D esistente per la modifica, l'aggiunta o l'elaborazione.
---
##  **Panoramica**
L'articolo spiega i seguenti argomenti utilizzando la libreria di manipolazione dei formati di file C# 3D.
- Crea una scena vuota 3D in C# da zero
- Leggi o carica la scena esistente di 3D in C#
- Salva la scena 3D in formati 3D supportati utilizzando C#
- Lavora con 3D proprietà scena in C#

##  **Crea una scena vuota 3D e risparmia nei formati file supportati 3D**
Aspose.3D API supporta la creazione delle nuove scene 3D da zero e quindi il salvataggio in qualsiasi formato di file supportato. Gli sviluppatori possono anche caricare una scena 3D esistente per la modifica, l'aggiunta o l'elaborazione.

###  **Creazione di un documento di scena 3D**
Segui questi passaggi in C# per creare un documento di scena 3D utilizzando l'API Aspose.3D:

1. Crea un'istanza della classe [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) che rappresenta un documento di scena 3D.
1. Genera un documento di scena 3D chiamando il metodo [`Save`](https://reference.aspose.com/3d/net/aspose.threed/scene/methods/save) dell'oggetto classe Scene.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-CreateEmpty3DDocument-CreateEmpty3DDocument.cs" >}}

##  **Lettura di una scena da 3D**
Utilizzando Aspose.3D API, gli sviluppatori possono caricare tutti i documenti 3D supportati. I costruttori disponibili della classe `Scene` consentono di farlo e accettano una stringa di percorso file valida. I formati di file leggibili supportati sono i seguenti:

1. FBX 7.5 (ASCII, binario)
1. FBX 7.4 (ASCII, binario)
1. FBX 7.3 (ASCII, binario)
1. FBX 7.2 (ASCII, binario)
1. FBX 6.1 (ASCII, binario)
1. STL (ASCII, binario)
1. WavefrontOBJ
1. Discreet3DS
1. Universal3D
1. Collada
1. glTF (ASCII, binario)
1. Maya (ASCII, binario)
1. OpenUSD (USD, USDZ)
1. Frullatore
1. DXF
1. PLY (ASCII, binario)
1. X (ASCII, binario)
1. Draco
1. 3MF
1. RVM (testo, binario)
1. ASE

I costruttori della classe `Scene` rilevano internamente il formato del documento 3D.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-ReadExistingScene-ReadExistingScene.cs" >}}

##  **Lavorare con 3D Proprietà scena**
Aspose.3D API ti consente di leggere 3D proprietà della scena utilizzando i nodi figlio della scena. Il seguente esempio di codice C# dimostra l'utilizzo di questa funzione.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-3DScene-ThreeDProperties-ThreeDProperties.cs" >}}
