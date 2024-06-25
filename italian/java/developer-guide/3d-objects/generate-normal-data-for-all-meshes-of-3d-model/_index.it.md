---
title: Generare dati normali per tutte le maglie del modello 3D
type: docs
weight: 40
url: /it/java/generate-normal-data-for-all-meshes-of-3d-model/
description: Aspose.3D for Java API supporta la generazione di dati normali per tutte le mesh del modello 3D (senza i dati normali).
---
{{% alert color="primary" %}} 

Aspose.3D for Java API supporta la generazione di dati normali per tutte le mesh del modello 3D (senza i dati normali).

{{% /alert %}} 
##  **Generare dati normali per tutte le maglie del modello 3DS**
Il metodo generateNormal esposto dalla classe `PolygonModifier` può essere utilizzato per generare dati normali per tutte le mesh in un file 3DS. Se l'elemento VertexElementSmoothingGroup è stato definito nella mesh, i dati normali generati verranno smussati da VertexElementSmoothingGroup.
###  **Campione di programmazione**
Questo esempio di codice carica un file 3DS, visita tutti i nodi e crea dati normali per tutte le mesh.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-objects-GenerateDataForMeshes.java" >}}
