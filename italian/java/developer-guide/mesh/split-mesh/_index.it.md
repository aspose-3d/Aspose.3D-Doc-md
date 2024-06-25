---
title: Rete spaccata
type: docs
weight: 10
url: /it/java/split-mesh/
description: Aspose.3D for Java API supporta la suddivisione di tutte le maglie di una scena in diverse mesh secondarie per materiale. Il metodo SplitMesh non dividerà una mesh della scena, se gli è stato assegnato un singolo materiale. Può essere ottenuto utilizzando Aspose.3D for Java API.
---
##  **Dividi tutte le maglie della scena per materiale**
Aspose.3D for Java API supporta la suddivisione di tutte le maglie di una scena in diverse mesh secondarie per materiale. Il metodo SplitMesh non dividerà una mesh della scena, se gli è stato assegnato un singolo materiale. Può essere ottenuto utilizzando Aspose.3D for Java API.

{{% alert color="primary" %}} 

`SplitMeshPolicy` enum specifica la politica dei dati utilizzata nell'algoritmo di frazionamento mesh, supporta due criteri, condividi i dati tra sottogruppi o ogni sottorete ha i propri dati (solo dati utilizzati).

{{% /alert %}} 

Il codice di esempio seguente divide tutte le mesh di una scena per materiale. Ogni sottogmesh condivide gli stessi dati diretti e differisce solo negli indici.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-mesh-SplitAllMeshesofScenebyMaterial.java" >}}
##  **Dividi una maglia specificando il materiale**
Aspose.3D for Java API supporta la divisione di una mesh specificando manualmente il materiale. L'opzione split mesh crea oggetti separati e ogni sottogmesh utilizzerà un solo materiale.
###  **Rete spaccata della scatola**
Questo argomento di aiuto crea una mesh della casella per mantenere il codice completo e breve. Gli sviluppatori possono costruire una mesh manualmente come narrato in questo argomento di aiuto: [Crea una mesh cubica da 3D](https://docs.dynabic.com/display/3djava/Create+3D+Mesh+and+Scene). Inoltre, una scatola è composta da 6 aerei e ogni aereo diventerà una sub mesh. Il codice di esempio seguente divide una mesh primitiva specificando manualmente il materiale.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-mesh-SplitMeshbyMaterial.java" >}}
