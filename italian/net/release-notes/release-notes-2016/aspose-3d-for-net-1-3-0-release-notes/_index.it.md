---
title: Aspose.3D for .NET 1.3.0 Note di rilascio
type: docs
weight: 100
url: /it/net/aspose-3d-for-net-1-3-0-release-notes/
---
## **Altri miglioramenti e modifiche**

|**Chiave** |**Riassunto** |**Categoria** |
|:- |:- |:- |
|THREEDNET-127 |Supporto di lettura del formato Universal 3D.|Nuova funzione|
|THREEDNET-133 |Verificare che gli spazi dei nomi Aspose.3D siano conformi alle linee guida Microsoft.|Miglioramento|
|THREEDNET-130 |Fix Aspose problema di abuso di licenza probabilmente causato da Aspose Ventures.|Bug|
### **Pubblico API e modifiche incompatibili arretrate**
Vedere l'elenco per eventuali modifiche apportate al pubblico API come membri aggiunti, rinominati, rimossi o deprecati, nonché qualsiasi modifica non compatibile con le versioni precedenti apportata allo Aspose.3D for .NET. Se hai dubbi su eventuali modifiche elencate, sollevalo sul[Forum di supporto Aspose.3D](https://forum.aspose.com/c/3d/18).
#### **Lo spazio dei nomi e il nome della classe cambiano:**
- Spazio dei nomi Aspose.ThreeD. Animazioni cambiate in Aspose.ThreeD. Animazione
- Classe Aspose.ThreeD. Animazioni. Animazione cambiata in Aspose.ThreeD.Animation.AnimationNode
- Namespace Aspose.ThreeD.IO cambiato in Aspose.ThreeD. Formati
- Namespace Aspose.ThreeD. Utili cambiati in Aspose.ThreeD.Utilities
#### **Cambiamenti funzionali:**
- Aggiunto un metodo di decomposizione su Matrix4
- Consentire all'utente di scomporre la matrice di trasformazione in traduzione/ridimensionamento/rotazione/inclinazione/prospettiva.
- Aggiunto un nuovo Constructor su Vector4 per ricevere un parametro Vector3.
- Rendere più facile costruire un Vector4 basato su un Vector3.
- Aggiunto un nuovo sovraccarico per Geometry.CreateElement and Geometry.CreateElementUV
- Consente all'utente di creare un nuovo elemento vertice e assegnare contemporaneamente la modalità di riferimento/modalità di mappatura, per rendere il codice più breve.
- Tipo modificato di LayeredTexture.Textures da ICollection a IList
- Consenti all'utente di accedere alle trame stratificate per indice.
- Aggiunta proprietà Contenuto in Texture
- Consentire all'utente di incorporare i dati di texture grezza all'interno dell'istanza Texture per i file FBX.
#### **Crea Vertex assegnando le modalità di riferimento e di mappatura**
Gli sviluppatori possono creare vertici assegnando le modalità di riferimento e mappatura in una singola riga di codice. Esempio di codice:[Imposta normali o UV sul cubo](/3d/it/net/set-up-normals-or-uv-on-the-cube-and-add-material-to-3d-entities/).
#### **Universal 3D L'opzione di salvataggio viene aggiunta nel FileFormat**
L'opzione del formato Universal 3D è stata aggiunta nell'enum FileFormat.
#### **Incorporare il contenuto grezzo alla trama dello FBX**
Il<tt>Contenuto</tt>La proprietà è stata aggiunta alla<tt>Texture</tt>Classe per incorporare il contenuto grezzo nella texture del documento FBX. Esempio di codice:[Aggiungere materiale al cubo](/3d/it/net/set-up-normals-or-uv-on-the-cube-and-add-material-to-3d-entities/#SetupnormalsorUVontheCubeandAddmaterialtothecube-Addmaterialtothecube).
#### **Il metodo di decomposizione viene aggiunto nella classe Matrix4**
È una funzione di utilità matematica utilizzata per decomporre una matrice di trasformazione affine.
#### **Un nuovo costruttore nella classe Vector4 viene aggiunto per ricevere un parametro oggetto Vector3**
Rende più facile costruire un Vector4 basato su Vector3. Il quarto valore del Vector4 presenta il piano w e il suo valore predefinito è 1.
