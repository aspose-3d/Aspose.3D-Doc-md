---
title: Crea e leggi una scena 3D esistente
type: docs
weight: 10
url: /it/python-net/create-and-read-an-existing-3d-scene/
description: Aspose.3D API supporta la creazione delle nuove scene 3D da zero e quindi il salvataggio in qualsiasi formato di file supportato. Gli sviluppatori possono anche caricare una scena 3D esistente per la modifica, l'aggiunta o l'elaborazione.
---
##  **Crea una scena vuota 3D e risparmia nei formati file supportati 3D**
Aspose.3D API supporta la creazione delle nuove scene 3D da zero e quindi il salvataggio in qualsiasi formato di file supportato. Gli sviluppatori possono anche caricare una scena 3D esistente per la modifica, l'aggiunta o l'elaborazione.
###  **Creazione di un documento di scena 3D**
Segui questi passaggi per creare un documento di scena 3D utilizzando le API Aspose.3D:

1. Crea un'istanza della classe [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene) che rappresenta un documento di scena 3D.
1. Genera un documento di scena 3D chiamando il metodo [`Save`](https://reference.aspose.com/3d/net/aspose.threed/scene/methods/save) dell'oggetto classe Scene.
####  **Creazione di un documento di scena 3D: campioni di programmazione**


{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-CreateEmpty3DDocument.py" >}}
##  **Lettura di una scena da 3D**
Utilizzando Aspose.3D API, gli sviluppatori possono caricare tutti i documenti 3D supportati. I costruttori disponibili del**Scena**La classe consente di farlo e accettano una stringa di percorso di file valida. I formati di file leggibili supportati sono i seguenti:

1. FBX 7.7 (ASCII, binario)
1. FBX 7.6 (ASCII, binario)
1. FBX 7.5 (ASCII, binario)
1. FBX 7.4 (ASCII, binario)
1. FBX 7.3 (ASCII, binario)
1. FBX 7.2 (ASCII, binario)
1. STL (ASCII, binario)
1. WavefrontOBJ
1. Discreet3DS
1. Universal3D
1. Collada
1. glTF
1. DXF
1. PLY (ASCII, binario)
1. X (ASCII, binario)
1. XYZ
1. Draco
1. 3MF
1. RVM (testo, binario)
1. ASE
1. USDZ
1. USD

I costruttori della classe `Scene` rilevano internamente il formato del documento 3D.
###  **Lettura di una scena da 3D: campioni di programmazione**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-ReadExistingScene.py" >}}
