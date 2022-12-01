---
title: Elenco delle caratteristiche
type: docs
weight: 30
url: /it/python-net/feature-list/
---
Caratteristiche Aspose.3D


## **Piattaforme supportate**

Le piattaforme Aspose.3D per Python via .NET possono essere utilizzate su Windowsx64 o x86 e un'ampia gamma di distribuzioni Linux con Python 3.5 o successive installate. Ci sono requisiti aggiuntivi per la piattaforma target Linux:
- GCC-6 librerie runtime (o successive)
- Dipendenze di .NET Core Runtime. L'installazione dello .NET Core Runtime stesso NON è richiesta
- Per Python 3.5-3.7: è necessaria la build pymalloc di Python. L'opzione di build -- with-pymalloc Python è abilitata per impostazione predefinita. In genere, la build pymalloc di Python è contrassegnata con il suffisso m nel nome file.
- Libpython ha condiviso la libreria Python. L'opzione di build-enable-shared Python è disabilitata per impostazione predefinita, alcune distribuzioni Python non contengono la libreria condivisa libpython. Per alcune piattaforme Linux, la libreria condivisa libpython può essere installata utilizzando il gestore di pacchetti, ad esempio: sudo apt-get install libpython3.7. Il problema comune è che la libreria libpython è installata in una posizione diversa rispetto alla posizione di sistema standard per le librerie condivise. Il problema può essere risolto utilizzando le opzioni di build Python per impostare percorsi di libreria alternativi durante la compilazione dello Python o risolto creando un collegamento simbolico al file della libreria libpython nella posizione standard di sistema per le librerie condivise. In genere, il nome del file della libreria condivisa libpython è libpythonX.Ym.so.1.0 per Python 3.5-3.7, o libpythonX.Y.so.1.0 per Python 3.8 o successivo (ad esempio: libpython3.7m.so.1.0, libpython3.9.so.1.0).
- Libgdiplus 6.0.1 o successivo


## **Matrice caratteristica**

|**Caratteristiche** |` `FBX|` `Collada|` `glTF|` `glTF 2.0|` `U3D|` `PDF|` `STL|` `OBJ|` `PLY|` `3DS|` `ASE|` `X|` `3MF|` `RVM|` `Draco|
|:- |:- |:- |:- |:- |:- |:- |:- |:- |:- |:- |:- |:- |:- |:- |:- |
|Materiale Lambert ` `|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>||<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>||<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>||<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>||||
|Materiale Phong ` `|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>||<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>||<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>|||<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>||||
|Materiale basato su shader ` `|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>||<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>|||||||||||||
|Materiale ` `PBR||||<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>||||||||||||
|Materiale speculare ` `PBR||||<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>||||||||||||
|` ` texture diffusa|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>||<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>||<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>||<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>|||
|` ` Trama avanzata|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>||<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>||<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>||||||||
|` ` mesh poligonate|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>||||||<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>||||||<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>||
|` `mesh a base di Triangolo|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>|
|` ` Elementi di vertice|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>||<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>|||<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>|
|` ` Geometrie NURBS|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>|||||||||||||||
|` ` Geometrie parametrizzate||||||||||||||<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>||
|` ` Trasformazione locale|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>||||<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>||<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>||
|` ` Installazione|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>||||||||||
|` ` Grafico di scena|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>||||<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>||<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>||<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>||
|` ` Proprietà personalizzata|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>||<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>||||||||||||
|` ` Scheletro|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>||||||||||||||
|` ` Deformatore Morph|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>||||||||||||||
|` ` Animazione della proprietà|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>||||||||||||||
|Compressione della maglia ` `|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>||||<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>|<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>|||||||<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>||<p>![Todo: immagine_Alt_Testo](accept.png)</p><p> </p>|

