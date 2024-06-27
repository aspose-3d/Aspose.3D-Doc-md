---
title: Generare dati normali per tutte le maglie in un file 3D
type: docs
weight: 70
url: /it/python-net/generate-normal-data-for-all-meshes-in-a-3d-file/
description: Utilizzando Aspose.3D for Python via .NET, gli sviluppatori possono generare dati normali per tutte le mesh in qualsiasi modello 3D (senza i dati normali).
---
{{% alert color="primary" %}}

Utilizzando [Aspose.3D for Python via .NET](https://products.aspose.com/3d/python-net/), gli sviluppatori possono generare dati normali per tutte le mesh in qualsiasi modello 3D (senza i dati normali).

{{% /alert %}}
##  **Generare dati normali per tutte le maglie in un file 3DS**
Il metodo `generate_normal` esposto dalla classe [`PolygonModifier`](https://reference.aspose.com/3d/net/aspose.threed.entities/polygonmodifier) può essere utilizzato per generare dati normali per tutte le mesh in un file 3DS. Se l'elemento `VertexElementSmoothingGroup` è stato definito nella mesh, i dati normali generati verranno smussati da `VertexElementSmoothingGroup`.
###  **Campione di programmazione**
Questo esempio di codice carica un file 3DS, visita tutti i nodi e crea dati normali per tutte le mesh.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Working-with-Objects-GenerateDataForMeshes-GenerateDataForMeshes.py" >}}
