---
title: Generare dati normali per tutte le maglie in un file 3D
type: docs
weight: 70
url: /it/net/generate-normal-data-for-all-meshes-in-a-3d-file/
description: Utilizzando Aspose.3D for .NET, gli sviluppatori possono generare dati normali per tutte le mesh in qualsiasi modello 3D (senza i dati normali).
---
{{% alert color="primary" %}}

Utilizzo[Aspose.3D for .NET](https://products.aspose.com/3d/net/), Gli sviluppatori possono generare dati normali per tutte le mesh in qualsiasi modello 3D (senza i dati normali).

{{% /alert %}}
## **Generare dati normali per tutte le maglie in un file 3DS**
Il metodo `GenerateNormal` esposto dalla classe [`PolygonModifier`](https://reference.aspose.com/3d/net/aspose.threed.entities/polygonmodifier) può essere utilizzato per generare dati normali per tutte le mesh in un file 3DS. Se l'elemento `VertexElementSmoothingGroup` è stato definito nella mesh, i dati normali generati verranno smussati dallo `VertexElementSmoothingGroup`.
### **Campione di programmazione**
Questo esempio di codice carica un file 3DS, visita tutti i nodi e crea dati normali per tutte le mesh.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Working-with-Objects-GenerateDataForMeshes-GenerateDataForMeshes.cs" >}}
