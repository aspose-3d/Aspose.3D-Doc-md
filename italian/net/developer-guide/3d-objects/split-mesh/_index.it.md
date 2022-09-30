---
title: Rete spaccata
type: docs
weight: 100
url: /it/net/split-mesh/
description: Gli sviluppatori possono richiedere di dividere tutte le maglie di una scena in più sottogruppi per materiale. Il metodo SplitMesh non dividerà una mesh della scena Se è stato assegnato un singolo materiale. Gli sviluppatori possono ora raggiungere questo obiettivo utilizzando Aspose.3D for .NET API.
---
## **Dividi tutte le maglie di una scena per materiale**
Gli sviluppatori possono richiedere di dividere tutte le maglie di una scena in più sottogruppi per materiale. Il metodo SplitMesh non dividerà una mesh della scena Se è stato assegnato un singolo materiale. Gli sviluppatori possono ora raggiungere questo obiettivo utilizzando[Aspose.3D for .NET](https://products.aspose.com/3d/net/)API.

{{% alert color="primary" %}}

`SplitMeshPolicy` enum specifica la politica dei dati utilizzata nell'algoritmo di frazionamento mesh, supporta due criteri, condividi i dati tra sottogmesh o ogni sottogmesh ha i propri dati (solo dati utilizzati).

{{% /alert %}}

Il codice di esempio seguente divide tutte le mesh di una scena per materiale. Ogni sottogmesh condivide gli stessi dati diretti e differisce solo negli indici.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Working-with-Objects-SplitAllMeshesofScenebyMaterial-SplitAllMeshesofScenebyMaterial.cs" >}}
## **Dividi una maglia specificando il materiale**
Aspose.3D for .NET API consente agli sviluppatori di dividere una mesh specificando manualmente il materiale. L'opzione split mesh crea oggetti separati e ogni sottogmesh utilizzerà un solo materiale.
### **Dividi la maglia della scatola**
Questo argomento di aiuto crea una mesh della casella per mantenere il codice completo e breve. Gli sviluppatori possono costruire una mesh manualmente come narrato in questo argomento di aiuto:[Creare una maglia cubica 3D](/3d/it/net/create-3d-mesh-and-scene/). Inoltre, una scatola è composta da 6 aerei e ogni aereo diventerà una sub mesh. Il codice di esempio seguente divide una mesh primitiva specificando manualmente il materiale.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Working-with-Objects-SplitMeshbyMaterial-SplitMeshbyMaterial.cs" >}}
