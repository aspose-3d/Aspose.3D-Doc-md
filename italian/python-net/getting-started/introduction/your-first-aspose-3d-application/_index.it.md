---
title: La tua prima applicazione Aspose.3D
type: docs
weight: 30
url: /it/python-net/your-first-aspose-3d-application/
---

{{% alert color="primary" %}}

Questa guida spiega come creare la tua prima applicazione utilizzando l'API semplice di Aspose.3D. Questa applicazione elementare crea un file 3D all'interno di una scena 3D specificata.

{{% /alert %}}

## **Come Creare l'Applicazione**

I passaggi seguenti illustrano come creare l'applicazione utilizzando l'API di Aspose.3D:

1. Creare un'istanza della classe [Scene](https://reference.aspose.com/3d/it/python-net/aspose.threed/scene/).
1. Se si dispone di una licenza, [applicarla](/3d/it/python-net/licensing/).
   Se si utilizza la versione di valutazione, saltare le righe di codice relative alla licenza.
1. Creare un nuovo file 3D oppure aprire un file 3D esistente.
1. Accedere ai contenuti della scena all'interno del file 3D.
1. Generare il file 3D modificato.

L'implementazione dei passaggi sopra indicati è illustrata negli esempi seguenti.

### **Come Creare un Nuovo Documento di Scena**

L'esempio seguente mostra come creare un nuovo file 3D da zero. Per prima cosa viene creata una scena 3D e successivamente il file viene salvato in formato FBX.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-CreateEmpty3DDocument.py" >}}

### **Come Aprire un File Esistente**

L'esempio seguente mostra come aprire un file 3D esistente denominato "document.fbx".

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-ReadExistingScene.py" >}}
