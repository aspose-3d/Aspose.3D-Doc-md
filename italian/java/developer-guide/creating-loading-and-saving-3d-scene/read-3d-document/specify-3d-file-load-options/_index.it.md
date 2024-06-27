---
title: Specificare 3D Opzioni di caricamento file
type: docs
weight: 10
url: /it/java/specify-3d-file-load-options/
description: Esistono diversi overload del metodo Scene.open o overload del costruttore di classi Scene che accettano l'istanza LoadOptions.
---
##  **3D Opzioni di caricamento file**
Esistono diversi overload del metodo Scene.open o overload del costruttore di classi Scene che accettano l'istanza LoadOptions. Questa dovrebbe essere un'istanza di una classe derivata dalla classe LoadOptions. Ogni formato di carico ha una classe corrispondente che contiene le opzioni di carico per quel formato di carico, ad esempio c' è ColladaSaveOptions per il formato di salvataggio FileFormat.COLLADA.
###  **Utilizzo delle opzioni di carico discre 3DS**
Il codice seguente mostra come impostare le opzioni di carico prima di caricare un file Discreet 3DS.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-Discreet3DSLoadOption.java" >}}
###  **Utilizzo delle opzioni di carico Obj**
Il codice seguente mostra come impostare le opzioni di carico prima di caricare un file Obj 3D.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-OBJLoadOption.java" >}}
###  **Utilizzo delle opzioni di carico STL**
Il codice seguente mostra come impostare le opzioni di carico prima di caricare un file STL.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-STLLoadOption.java" >}}
###  **Utilizzo delle opzioni di carico U3D**
Il codice seguente mostra come impostare le opzioni di carico prima di caricare un file U3D.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-U3DLoadOption.java" >}}
###  **Utilizzo delle opzioni di carico glTF**
Il codice seguente mostra come impostare le opzioni di carico prima di caricare un file glTF.
####  **Capovolgi la Coordinata texture V/T**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-glTFLoadOptions.java" >}}
###  **Utilizzo delle opzioni di carico Ply**
Il codice seguente mostra come impostare le opzioni di carico prima di caricare un modello PLY.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-PLYLoadOption.java" >}}
###  **Utilizzo delle opzioni di carico DirectX X**
Il codice seguente mostra come impostare le opzioni di carico prima di caricare un file DirectX X.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-loadsave-XLoadOption.java" >}}
###  **Utilizza FBX opzioni di carico**
{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-loadsave-LoadOptions-FBXLoadOptions.java" >}}
