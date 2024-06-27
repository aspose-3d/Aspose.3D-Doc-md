---
title: Rete spaccata
type: docs
weight: 100
url: /it/python-net/split-mesh/
description: Gli sviluppatori possono richiedere di dividere tutte le maglie di una scena in più sottogruppi per materiale. Il metodo SplitMesh non dividerà una mesh della scena Se è stato assegnato un singolo materiale. Gli sviluppatori possono ora raggiungere questo obiettivo utilizzando Aspose.3D for Python via .NET API.
---
##  **Dividi tutte le maglie di una scena per materiale**
Gli sviluppatori possono richiedere di dividere tutte le maglie di una scena in più sottogruppi per materiale. Il metodo `split_mesh` non dividerà una mesh della scena Se è stato assegnato un singolo materiale. Gli sviluppatori possono ora raggiungere questo obiettivo utilizzando [Aspose.3D for Python via .NET](https://products.aspose.com/3d/python-net/) API.

{{% alert color="primary" %}}

`SplitMeshPolicy` enum specifica la politica dei dati utilizzata nell'algoritmo di frazionamento mesh, supporta due criteri, condividi i dati tra sottogruppi o ogni sottorete ha i propri dati (solo dati utilizzati).

{{% /alert %}}

Il codice di esempio seguente divide tutte le mesh di una scena per materiale. Ogni sottogmesh condivide gli stessi dati diretti e differisce solo negli indici.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-SplitAllMeshesofScenebyMaterial-SplitAllMeshesofScenebyMaterial.py" >}}
##  **Dividi una maglia specificando il materiale**
Aspose.3D for Python via .NET API consente agli sviluppatori di dividere una mesh specificando manualmente il materiale. L'opzione split mesh crea oggetti separati e ogni sottogmesh utilizzerà un solo materiale.
###  **Dividi la maglia della scatola**
Questo argomento di aiuto crea una mesh della casella per mantenere il codice completo e breve. Gli sviluppatori possono costruire una mesh manualmente come narrato in questo argomento di aiuto: [Crea una mesh cubica da 3D](/3d/it/python-net/create-3d-mesh-and-scene/). Inoltre, una scatola è composta da 6 aerei e ogni aereo diventerà una sub mesh. Il codice di esempio seguente divide una mesh primitiva specificando manualmente il materiale.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-SplitMeshbyMaterial-SplitMeshbyMaterial.py" >}}
