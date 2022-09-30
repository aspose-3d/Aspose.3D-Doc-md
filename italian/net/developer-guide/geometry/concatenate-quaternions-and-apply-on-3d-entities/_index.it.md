---
title: Concatenare quaternioni e applicare su 3D entità
type: docs
weight: 50
url: /it/net/concatenate-quaternions-and-apply-on-3d-entities/
description: Aspose.3D for .NET consente agli sviluppatori di combinare due trasformazioni di rotazione in una rappresentata in un quaternione.
---
{{% alert color="primary" %}} 

[Aspose.3D for .NET](https://www.aspose.com/products/3d)Consente agli sviluppatori di combinare due trasformazione di rotazione in una rappresentata in un quaternione.

{{% /alert %}} 
## **Concatenati quaternioni**
I quaternioni sono usati per rappresentare un orientamento nello spazio 3D. Il metodo `Concat` esposto dalla classe [`Quaternion`](https://reference.aspose.com/3d/net/aspose.threed.utilities/quaternion) può essere utilizzato per combinare due quaternioni. In questo esempio di codice, combiniamo due quaternioni e otteniamo un terzo quaternione risultante, quindi applichiamo questi tre quaternioni a tre cilindri.
### **Campione di programmazione**
Questo esempio di codice combina due quaternioni e li applica a diversi cilindri.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Geometry-and-Hierarchy-ConcatenateQuaternions-ConcatenateQuaternions.cs" >}}


**Risultato in 3ds MAX**

![Todo: immagine_Alt_Testo](concatenate-quaternions-and-apply-on-3d-entities_1.png)
