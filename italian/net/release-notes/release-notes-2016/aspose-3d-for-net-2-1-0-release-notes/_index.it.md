---
title: Aspose.3D for .NET 2.1.0 Note di rilascio
type: docs
weight: 40
url: /it/net/aspose-3d-for-net-2-1-0-release-notes/
---
{{% alert color="primary" %}} 

Questa pagina contiene le note di rilascio per[Aspose.3D for .NET 2.1.0](https://www.nuget.org/packages/Aspose.3D/2.1.0).

{{% /alert %}} 
## **Altri miglioramenti e modifiche**

|**Chiave**|**Riassunto**|**Categoria**|
|:- |:- |:- |
|THREEDNET-196|Opzioni di importazione separate ed opzioni di esportazione per tutti i formati di file 3D.|Nuova funzione|
|THREEDNET-194|Sostegno all'esportazione per Collada.|Nuova funzione|
|THREEDNET-198|Consentire all'utente di accedere al rendering di basso livello API.|Nuova funzione|
|THREEDNET-199|Consentire l'esclusione del nodo durante l'esportazione.|Miglioramento|
|THREEDNET-195|Display texture non trovato sul modello.|Miglioramento|
|THREEDNET-203|Consentire la modificabilità di Vector2/Vector3/Vector4/Quaternion nella griglia delle proprietà.|Miglioramento|
|THREEDNET-197|Questione di triangola poligonale.|Bug|
|THREEDNET-202|Diffuse/speculari/Emissive non funzionerà se non viene utilizzata alcuna texture.|Bug|
### **Pubblico API e modifiche incompatibili arretrate**
Vedere l'elenco per eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non compatibile con le versioni precedenti apportata allo Aspose.3D for .NET. Se hai dubbi su eventuali modifiche elencate, sollevalo sul[Forum di supporto Aspose.3D](https://forum.aspose.com/c/3d/18).
#### **Aggiunge Esportazione del formato Collada**
Utilizzando questa versione recente (2.1.0), gli sviluppatori possono esportare i file Collada 3D. Nella versione precedente (2.0.0), abbiamo già aggiunto la sua funzione di importazione, poiché gli sviluppatori possono anche convertire un file Collada in altri formati di file 3D supportati.
### **Aggiunge opzioni di carico e salvataggio per i formati di file 3D**
Abbiamo aggiunto opzioni di carico e salvataggio per ogni formato di file. Sono rifattorizzati dalle sottoclassi IOConfig originali.
#### **Aggiunge Aspose.ThreeD. Formati. ColladaSaveOptions/Discreet3DSLoadOptions/Discreet3DSSaveOptions/FBXSaveOptions/ObjLoadOptions/ObjSaveOptions/STLLoadOptions/U3DLoadOptions/U3DSaveOptions**
1. **Classe ColladaSaveOptions**-Definisce le impostazioni sul salvataggio di un file Collada 3D.
1. **Classe Discreet3DSLoadOptions**-Definisce le impostazioni sul caricamento di un discreto file 3DS.
1. **Classe Discreet3DSSaveOptions**-Definisce le impostazioni sul salvataggio di un discreto file 3DS.
1. **Classe FBXSaveOptions**-Definisce le impostazioni sul salvataggio di un file FBX.
1. **Classe ObjLoadOptions**-Definisce le impostazioni sul caricamento di un file Obj.
1. **Classe ObjSaveOptions**-Definisce le impostazioni sul salvataggio di un file Obj.
1. **Classe STLLoadOptions**-Definisce le impostazioni sul caricamento di un file STL.
1. **Classe STLSaveOptions**-Definisce le impostazioni sul salvataggio di un file STL.
1. **Classe U3DLoadOptions**-Definisce le impostazioni sul caricamento di un file U3D.
1. **Classe U3DSaveOptions**-Definisce le impostazioni sul salvataggio di un file U3D.

{{% alert color="primary" %}} 

Le vecchie sottoclassi IOConfig sono contrassegnate come obsolete, verranno rimosse nella prossima versione principale (3.0.0).

{{% /alert %}} 
### **Aggiunge metodi a Aspose.ThreeD. Classe scena**
Abbiamo sovraccaricato i metodi Open and Save nella classe Scene. Gli sviluppatori possono passare un oggetto stream o un nome file diretto per importare/esportare un file 3D utilizzando le varie opzioni di caricamento/salvataggio.
### **Rimozione della proprietà FillDummyIndexArray da Aspose.ThreeD.Formats.FBXConfig Class**
Questa proprietà non veniva utilizzata.
### **Rilevare il tipo di un file 3D**
Il metodo Rileva della classe Aspose.ThreeD.FileFormat è in grado di riconoscere il tipo di qualsiasi file 3D supportato.
#### **Aggiunge Rileva, CreateLoadOptions e CreateSaveOptions Metodi nella classe Aspose.ThreeD.FileFormat**
Dopo il riconoscimento di un tipo di file 3D, gli sviluppatori possono creare oggetti LoadOptions e SaveOptions utilizzando i metodi CreateLoadOptions e CreateSaveOptions della classe FileFormat.
### **Aggiunge la proprietà esclusa a Aspose.ThreeD. Entità e Aspose.ThreeD. Classi di nodi**
Consente di rimuovere un'entità durante l'esportazione.
### **Aggiunge Aspose.ThreeD.Render.RenderState Class e Aspose.ThreeD.Render.BlendFactor/CompareFunction/CullFaceMode/FrontFace/PolygonMode/StencilAction/StencilState Enums**
Gli stati di rendering forniscono parametri per la GPU per rasterizzare i triangoli in pixel.

{{% alert color="primary" %}} 

Incapsulamento degli stati di rendering dell'hardware, informazioni dettagliate possono essere trovate nella documentazione di[OpenGL 4.0](https://www.opengl.org/sdk/docs/man/html/glEnable.xhtml), [DirectX 11](https://msdn.microsoft.com/en-us/library/windows/desktop/hh404489\(v=vs.85\). Aspx),[DirectX 9](https://msdn.microsoft.com/en-us/library/windows/desktop/bb147327\(v=vs.85\). Aspx) e[Vulkan](https://www.khronos.org/registry/vulkan/specs/1.0/xhtml/vkspec.html#VkPipelineRasterizationStateCreateInfo)

{{% /alert %}} 
### **Aggiunge API Shader**
Le API Shader definiscono come trasformare i triangoli dallo spazio del mondo nello spazio dello schermo e calcolare il colore finale del pixel sul lato GPU.
#### **Aggiunge una classe astratta Aspose.ThreeD.Render.ShaderSource e sottoclasse Aspose.ThreeD.Render.GLSLSource**
GLSLSource dice al renderer, il codice sorgente è per il linguaggio di ombreggiatura OpenGL, può essere compilato allo Aspose.ThreeD.Render.ShaderProgram.
#### **Aggiunge Aspose.ThreeD.Render.ShaderException Class**
Le eccezioni relative allo shader, utilizzate principalmente nella fase di compilazione e collegamento in lingua shader.
#### **Aggiunge Aspose.ThreeD.Render.ShaderProgram Class**
È il programma shader compilato.
#### **Aggiungi Aspose.ThreeD.Render.ShaderVariable Class**
Definisce le variabili utilizzate in shader.
#### **Aggiunge una classe Enum Aspose.ThreeD.Render.VariableSemantic**
Viene utilizzato per identificare la semantica della variabile shader, Aspose.3D renderer preparerà automaticamente i valori delle variabili shader a seconda della semantica.
### **Aggiunge API buffer**
I buffer forniscono definizione e dati dei triangoli.
#### **Aggiunge un'interfaccia Aspose.ThreeD.Render.IBuffer**
È l'interfaccia di base per IIndexBuffer e IVertexBuffer.
#### **Aggiunge interfacce Aspose.ThreeD.Render.IIndexBuffer/IVertexBuffer**
Presentano buffer hardware per la memorizzazione degli indici di geometria.
#### **Aggiunge un Enum Aspose.ThreeD.Render.IndexDataType**
Il tipo di dati degli indici di geometria.
### **Aggiunge le API di Render**
#### **Aggiunge un'interfaccia Aspose.ThreeD.Render. Irenderable**
Un oggetto che supporta il rendering dovrebbe implementare questa interfaccia.
#### **Aggiunto un Enum Aspose.ThreeD.Render. Drawoperation**
Il tipo primitivo da disegnare.
#### **Aggiunge un Enum Aspose.ThreeD.Render.RenderQueueGroupId**
Aspose.3D API utilizza la coda di rendering per gestire il flusso di lavoro di rendering, questo viene utilizzato per inviare l'operazione di rendering alla coda di rendering specificata.
#### **Aggiunge Aspose.ThreeD.Render. Renderce Resources Class**
Classe di base per collegare il modello Aspose.3D dello API alle risorse hardware, questa viene utilizzata internamente dallo Aspose.3D, ma esposta per liberare tutta la potenza del rendering Aspose.3D.
#### **Aggiunge Aspose.ThreeD.Render.RenderableResource Class**
Una sottoclasse di RenderResource, ma concentrati sul rendering.
#### **Aggiunge Aspose.ThreeD. Entità. ManualEntità Class**
L'utente deve utilizzare questa classe per implementare la propria entità che supporta il rendering, questa classe incapsula i dettagli delle operazioni di rendering e della gestione delle risorse.
### **Aggiunge più metodi triangolati nella classe Aspose.ThreeD.Entities.PolygonModifier**
Più sovraccarichi per semplificare l'utilizzo della funzione originale.
### **Aggiunge i metodi CreateVertexBuffer, CreateIndexBuffer, CreateTextureUnit, CreateRenderState e CreateShaderProgram nella classe Aspose.ThreeD.Render.RenderFactory**
### **Aggiunge i metodi BindRenderState, Drawexed, Draw e SubmitRenderTask nella classe Aspose.ThreeD.Render.Renderer**
### **Aggiunge le proprietà RenderStage e Shader nella classe Aspose.ThreeD.Render.Renderer**
