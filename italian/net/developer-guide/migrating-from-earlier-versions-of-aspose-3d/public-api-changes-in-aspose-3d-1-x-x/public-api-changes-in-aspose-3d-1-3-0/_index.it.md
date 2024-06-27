---
title: Variazioni pubbliche di API in Aspose.3D 1.3.0
type: docs
weight: 40
url: /it/net/public-api-changes-in-aspose-3d-1-3-0/
---
**Contenuto sommario**

- [Lo spazio dei nomi e il nome della classe cambiano](#PublicAPIChangesinAspose.3D1.3.0-Namespaceandclassnamechanges)
- [Crea Vertex assegnando le modalità di riferimento e di mappatura](#PublicAPIChangesinAspose.3D1.3.0-CreateVertexbyAssigningtheReferenceandMappingModes)
- [L'opzione di salvataggio di Universal 3D viene aggiunta nel FileFormat](#PublicAPIChangesinAspose.3D1.3.0-Universal3DSavingOptionisaddedintheFileFormat)
- [Incorpora il contenuto grezzo nella texture di FBX](#PublicAPIChangesinAspose.3D1.3.0-EmbedRawContenttotheTextureofFBX)
- [Il metodo di decomposizione viene aggiunto nella classe Matrix4](#PublicAPIChangesinAspose.3D1.3.0-DecomposemethodisaddedintheMatrix4class)
- [Un nuovo costruttore nella classe Vector4 viene aggiunto per ricevere un parametro oggetto Vector3](#PublicAPIChangesinAspose.3D1.3.0-AnewconstructorinVector4classisaddedtoreceiveaVector3objectparameter)

{{% alert color="primary" %}} 

Questo documento descrive le modifiche a Aspose.3D API dalla versione da 1.2.0 a 1.3.0, che potrebbero interessare gli sviluppatori di moduli/applicazioni. Include non solo metodi pubblici nuovi e aggiornati, ma anche una descrizione di eventuali cambiamenti nel comportamento dietro le quinte in Aspose.3D.

{{% /alert %}} 
###  **Lo spazio dei nomi e il nome della classe cambiano**
- Namespace Aspose.ThreeD. Animazioni cambiate in Aspose.ThreeD.Animation
- Classe Aspose.ThreeD. Animazioni. Animazione cambiata in Aspose.ThreeD.Animation.AnimationNode
- Namespace Aspose.ThreeD.IO cambiato in Aspose.ThreeD.Formats
- Namespace Aspose.ThreeD.Utils cambiato in Aspose.ThreeD.Utilities
###  **Crea Vertex assegnando le modalità di riferimento e di mappatura**
Gli sviluppatori possono creare vertici assegnando le modalità di riferimento e mappatura in una singola riga di codice. Esempio di codice:

{{% alert color="primary" %}} 

L'oggetto della classe Mesh viene utilizzato nel codice. Possiamo [Creare un oggetto classe Mesh come narrato lì](/pages/createpage.action?spaceKey=3dnet&title=Create+a+3D+Cube+Mesh&linkCreation=true&fromPageId=19923253).

{{% /alert %}} 

**C#**

{{< highlight "csharp" >}}

 // call overloaded CreateElement method of the Mesh object

VertexElementNormal elementNormal = mesh.CreateElement(VertexElementType.Normal, MappingMode.ControlPoint, ReferenceMode.Direct) as VertexElementNormal;

{{< /highlight >}}

###  **L'opzione di salvataggio di Universal 3D viene aggiunta nel FileFormat**
L'opzione di formato Universal 3D è stata aggiunta nell'enum FileFormat. Esempio di codice:

**C#**

{{< highlight "csharp" >}}

 // save scene in the Universal3D format

scene.Save("C:\\temp\\Output.fbx", FileFormat.Universal3D);

{{< /highlight >}}

###  **Incorpora il contenuto grezzo nella texture di FBX**
Il<tt>Contenuto</tt>La proprietà è stata aggiunta alla<tt>Texture</tt>Per incorporare il contenuto grezzo nella texture del documento FBX. Esempio di codice:

**C#**

{{< highlight "csharp" >}}

 // initialize Texture class object

Texture texture = new Texture();

// set file name

texture.FileName = "embedded-texture.png";

// set binary content

texture.Content = File.ReadAllBytes("c:\\test.png");

{{< /highlight >}}

###  **Il metodo di decomposizione viene aggiunto nella classe Matrix4**
È una funzione di utilità matematica utilizzata per decomporre una matrice di trasformazione affine.
###  **Un nuovo costruttore nella classe Vector4 viene aggiunto per ricevere un parametro oggetto Vector3**
Rende più facile costruire un Vector4 basato su Vector3. Il quarto valore del Vector4 presenta il piano w e il suo valore predefinito è 1.
