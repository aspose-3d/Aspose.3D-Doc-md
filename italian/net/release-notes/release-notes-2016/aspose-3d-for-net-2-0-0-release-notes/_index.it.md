---
title: Aspose.3D for .NET 2.0.0 Note di rilascio
type: docs
weight: 50
url: /it/net/aspose-3d-for-net-2-0-0-release-notes/
---
{{% alert color="primary" %}} 

Questa pagina contiene le note di rilascio per[Aspose.3D for .NET 2.0.0](https://www.nuget.org/packages/Aspose.3D/2.0.0).

{{% /alert %}} 
## **Altri miglioramenti e modifiche**

|**Chiave**|**Riassunto**|**Categoria**|
|:- |:- |:- |
|THREEDNET-113|Sostegno all'importazione per Collada|Nuova funzionalità|
|THREEDNET-183|Effetti post-elaborazione|Nuova funzionalità|
|THREEDNET-191|Usa Vector4 per rappresentare le coordinate UV.|Miglioramento|
|THREEDNET-189|Il render può bloccare l'applicazione sulla piattaforma a 64bit|Bug|
### **Pubblico API e modifiche incompatibili arretrate**
Vedere l'elenco per eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non compatibile con le versioni precedenti apportata allo Aspose.3D for .NET. Se hai dubbi su eventuali modifiche elencate, sollevalo sul[Forum di supporto Aspose.3D](https://forum.aspose.com/c/3d/18).
#### **Rendering in tempo reale**
Consente agli sviluppatori di eseguire il rendering in tempo reale ad alte prestazioni su un framework GUI come WinForms, è indipendente dal framework GUI, quindi anche gli altri framework GUI dovrebbero supportarlo.
#### **Aggiunge il formato Collada**
In questa versione (2.0.0), gli sviluppatori possono importare i file Collada 3D, quindi la proprietà Collada viene aggiunta in Aspose.ThreeD. Classe FileFormat
#### **Aggiunge Aspose.ThreeD.Utilities.BoundingBox e Aspose.ThreeD.Utilities.BoundingBoxExtent classi**
Le classi BoundingBox e BoundingBoxExtent rappresentano il riquadro di delimitazione di un nodo 3D. Gli sviluppatori possono reimpostare la fotocamera e calcolare l'elevazione dal riquadro di delimitazione. Il riquadro di delimitazione infinito o nullo significa che la scena non ha geometrie e regola l'elevazione della telecamera solo quando è finita.
#### **Rinominato tipo Aspose.ThreeD.UpVector allo Aspose.ThreeD.Axis**
La classe UpVector è stata rinominata in classe Axis.
#### **Aggiunge Aspose.ThreeD.Render.DriverException class**
Le eccezioni del renderer interno sono racchiuse come DriverException.
#### **Aggiunge Aspose.ThreeD.Render.InitializationException Class**
Questa eccezione viene generata mentre non si riesce a inizializzare il renderer, ad esempio per inizializzarlo su un computer che non ha supporto hardware di OpenGL 4.0.
#### **Aggiunge Aspose.ThreeD.Render.Renderer class**
Crea un oggetto Renderer e una finestra di rendering dalla maniglia nativa della finestra. Al momento supportiamo solo la maniglia finestra nativa dallo Microsoft Windows. Supporteremo più piattaforme in futuro. Il metodo CreateRenderer della classe Renderer crea un renderer backend OpenGL-hardware e verranno eseguite alcune inizializzazioni interne. Quando il renderer esce dall'ambito, verranno smaltite anche le risorse hardware non gestite.
#### **Aggiunge Aspose.ThreeD.Render.Viewport classe**
Aspose.3D API supporta tre tipi di visualizzazioni. Poiché il rendering è destinato a qualsiasi viewport di questi tipi.
#### **Aggiunge Aspose.ThreeD.Render.IRenderTarget/IRenderTexture/IRenderWindow classi**
- IRenderTarget è l'interfaccia di base di IRenderTexture/IRenderWindow.
- IRenderTexture consente di rendere la scena a una o più trame (le trame si trovano nella memoria video e possono essere trasferite nella memoria di sistema).
- IRenderWindow consente di rendere la scena in finestra in tempo reale.
#### **Aggiunge Aspose.ThreeD.Render.ITextureUnit e Aspose.ThreeD.Render.TextureType classi**
ITextureUnit è in realtà il campionatore di texture sul lato GPU e i dati di texture nella memoria CPU o GPU.
#### **Aggiunge Aspose.ThreeD.Render. classe di PostProcessing**
La classe PostProcessing consente agli sviluppatori di applicare il filtro di elaborazione delle immagini in tempo reale all'immagine renderizzata. In questa versione, abbiamo fornito 4 effetti di post-elaborazione integrati. Consentiremo agli sviluppatori di avere il proprio algoritmo di post-elaborazione personalizzato nella versione futura.
#### **Aggiunge Aspose.ThreeD.Render.RenderFactory classe**
Aiuta a rendere una scena su trame o finestre in tempo reale.
#### **Aggiunge Aspose.ThreeD.Render.RenderParameters class**
Definisce i parametri su come creare il target di rendering come bit di colore, bit di profondità, bit di stencil, doppio buffering.
#### **I metodi AddData sono aggiunti allo Aspose.ThreeD. Entità. Classe VertexElementUV**
La classe base di VertexElementUV è cambiata da VertexElementTemplate<Vector2>A VertexElementTemplate<Vector4>, Memorizzerà Vector4 solo da 2.0.0, quindi sono stati aggiunti due metodi di supporto per consentire all'utente di aggiungere un elenco di Vector2 e Vector3 a VertexElementUV, espanderà internamente Vector2/Vector3 a Vector4 e lascerà zero i campi rimanenti:
#### **Cambiamenti di proprietà nella classe Aspose.ThreeD.FileFormat**
Le proprietà di FileFormat vengono modificate da un numero intero a System.Version.
#### **Il metodo GetBoundingBox è aggiunto allo Aspose.ThreeD. Nodo**
Consente agli sviluppatori di ottenere il riquadro di delimitazione allineato all'asse.
