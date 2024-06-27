---
title: Triangolazione di un poligono semplice
type: docs
weight: 30
url: /it/python-net/triangulation-of-a-simple-polygon/
description: Utilizzando Aspose.3D for Python via .NET API, gli sviluppatori possono triangolare un semplice poligono. Qualsiasi poligono può essere diviso in triangoli. Tutte le operazioni e i calcoli per i triangoli possono essere applicati a tratti al poligono.
---
{{% alert color="primary" %}}

Utilizzando [Aspose.3D for Python via .NET](https://products.aspose.com/3d/python-net/) API, gli sviluppatori possono triangolare un semplice poligono. Qualsiasi poligono può essere diviso in triangoli. Tutte le operazioni e i calcoli per i triangoli possono essere applicati a tratti al poligono.

{{% /alert %}}
##  **Triangolazione di un poligono**
Gli sviluppatori potrebbero scegliere i vertici da un'area poligonale e quindi formare triangoli chiamando il metodo Triangulate della classe [`PolygonModifier`](https://reference.aspose.com/3d/net/aspose.threed.entities/polygonmodifier), ciascuna delle forme V{1}, V{i-1}, V{i} con l'indice i che va da 3 a n. Le classi `Vertex` e `PolygonCanvas` nel file `Triangulate/PolygonCanvas.py` sotto l'applicazione demo (nome: Triangulate) dimostrano il modo di triangolare un poligono usando Aspose.3D API.

{{% alert color="primary" %}}

Abbiamo preparato un progetto demo. Fai riferimento a [Questo URL](https://github.com/aspose-3d/Aspose.3D-for-.NET/tree/master/Demos).

{{% /alert %}}
###  **Campione di programmazione per la triangolazione**
Questo esempio di codice seleziona i vertici da un'area poligonale e quindi applica un algoritmo per creare triangoli. Puoi scaricare il progetto di lavoro completo di questo esempio da [Qui](https://github.com/aspose-3d/Aspose.3D-for-.NET/).

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "TriangulationSimplePolygon-Triangulate-PolygonCanvas-TriangulationofaSimplePolygon.py" >}}
