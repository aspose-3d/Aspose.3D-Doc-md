---
title: Creare e leggere una scena esistente 3D
type: docs
weight: 10
url: /it/net/create-and-read-an-existing-3d-scene/
description: Aspose.3D API supporta la creazione di nuove 3D scene da zero e quindi salvare in qualsiasi formato di file supportato. Gli sviluppatori possono anche caricare una scena 3D esistente per gli scopi di modifica, aggiunta o elaborazione.
---
## **Panoramica**
L'articolo spiega i seguenti argomenti utilizzando la libreria di manipolazione dei formati di file C# 3D.
- Creare una scena vuota 3D in C# da zero
- Leggi o carica la scena 3D esistente nello C#
- Salva la scena 3D nei formati supportati 3D utilizzando C#
- Lavora con 3D Proprietà della scena in C#

## **Creare una scena vuota 3D e salvare nei formati file supportati 3D**
Aspose.3D API supporta la creazione di nuove 3D scene da zero e quindi salvare in qualsiasi formato di file supportato. Gli sviluppatori possono anche caricare una scena 3D esistente per gli scopi di modifica, aggiunta o elaborazione.

### **Creazione di un documento di scena 3D**
Segui questi passaggi in C# per creare un documento della scena 3D utilizzando le API Aspose.3D:

1. Creare un'istanza della classe [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) che rappresenta un documento di scena 3D.
1. Generare un documento della scena 3D chiamando il metodo [`Save`](https://reference.aspose.com/3d/net/aspose.threed/scene/methods/save) dell'oggetto della classe Scene.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-CreateEmpty3DDocument-CreateEmpty3DDocument.cs" >}}

## **Lettura di una scena 3D**
Utilizzando Aspose.3D API, gli sviluppatori possono caricare tutti i documenti 3D supportati. I costruttori disponibili della classe `Scene` consentono di farlo e accettano una stringa di percorso di file valida. I formati di file leggibili supportati sono i seguenti:

1. FBX 7.5 (ASCII, Binario)
1. FBX 7.4 (ASCII, Binario)
1. FBX 7.3 (ASCII, Binario)
1. FBX 7.2 (ASCII, Binario)
1. STL (ASCII, Binario)
1. WavefrontOBJ
1. Discreet3DS
1. Universal3D
1. Collada
1. glTF
1. DXF
1. PLY (ASCII, Binario)
1. X (ASCII, Binario)
1. Draco
1. 3MF
1. RVM (Testo, binario)
1. ASE

I costruttori della classe `Scene` rilevano internamente il formato del documento 3D.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Loading-and-Saving-ReadExistingScene-ReadExistingScene.cs" >}}

## **Lavorare con le proprietà della scena 3D**
Aspose.3D API consente di leggere le proprietà della scena 3D utilizzando i nodi figlio della scena. Il seguente esempio di codice C# dimostra l'utilizzo di questa funzione.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-3DScene-ThreeDProperties-ThreeDProperties.cs" >}}
