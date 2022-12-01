---
title: Creare e leggere una scena esistente 3D
type: docs
weight: 10
url: /it/python-net/create-and-read-an-existing-3d-scene/
description: Aspose.3D API supporta la creazione di nuove 3D scene da zero e quindi salvare in qualsiasi formato di file supportato. Gli sviluppatori possono anche caricare una scena 3D esistente per gli scopi di modifica, aggiunta o elaborazione.
---
## **Creare una scena vuota 3D e salvare nei formati file supportati 3D**
Aspose.3D API supporta la creazione di nuove 3D scene da zero e quindi salvare in qualsiasi formato di file supportato. Gli sviluppatori possono anche caricare una scena 3D esistente per gli scopi di modifica, aggiunta o elaborazione.
### **Creazione di un documento di scena 3D**
Segui questi passaggi per creare un documento della scena 3D utilizzando le API Aspose.3D:

1. Creare un'istanza della classe [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) che rappresenta un documento di scena 3D.
1. Generare un documento della scena 3D chiamando il metodo [`Save`](https://reference.aspose.com/3d/net/aspose.threed/scene/methods/save) dell'oggetto della classe Scene.
#### **Creazione di un documento di scena 3D: campioni di programmazione**


{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-CreateEmpty3DDocument.py" >}}
## **Lettura di una scena 3D**
Utilizzando Aspose.3D API, gli sviluppatori possono caricare tutti i documenti 3D supportati. I costruttori disponibili del**Scena**La classe consente di farlo e accettano una stringa di percorso di file valida. I formati di file leggibili supportati sono i seguenti:

1. FBX 7.7 (ASCII, Binario)
1. FBX 7.6 (ASCII, Binario)
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
1. XYZ
1. Draco
1. 3MF
1. RVM (Testo, binario)
1. ASE
1. USDZ
1. USD

I costruttori della classe `Scene` rilevano internamente il formato del documento 3D.
### **Lettura di una scena 3D: campioni di programmazione**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-ReadExistingScene.py" >}}
