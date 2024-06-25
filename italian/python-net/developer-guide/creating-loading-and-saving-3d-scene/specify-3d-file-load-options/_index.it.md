---
title: Specificare 3D Opzioni di caricamento file
type: docs
weight: 30
url: /it/python-net/specify-3d-file-load-options/
description: Esistono diversi overload del metodo Scene.Open o overload del costruttore di classi Scene che accettano un oggetto LoadOptions. Ogni formato di carico ha una classe corrispondente che contiene le opzioni di carico per quel formato di carico.
---
##  **3D Opzioni di caricamento file**
Sono disponibili diversi overload del metodo [`Scene.open`](https://reference.aspose.com/3d/net/aspose.threed/scene) o overload del costruttore di classi Scene che accettano un oggetto `LoadOptions`. Questo dovrebbe essere un oggetto di una classe derivata dalla classe `LoadOptions`. Ogni formato di carico ha una classe corrispondente che contiene le opzioni di carico per quel formato di carico, ad esempio c' è `ColladaSaveOptions` per il formato di salvataggio `FileFormat.Collada`.
###  **Utilizzo delle opzioni di carico discre 3DS**
Il codice seguente mostra come impostare le opzioni di carico prima di caricare un file Discreet 3DS.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-Discreet3DSOption.py" >}}
###  **Utilizzo delle opzioni di carico Obj**
Il codice seguente mostra come impostare le opzioni di carico prima di caricare un file Obj 3D.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-ObjLoadOption.py" >}}
###  **Utilizzo delle opzioni di carico STL**
Il codice seguente mostra come impostare le opzioni di carico prima di caricare un file STL.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-STLLoadOption.py" >}}
###  **Utilizzo delle opzioni di carico U3D**
Il codice seguente mostra come impostare le opzioni di carico prima di caricare un file U3D.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-U3DLoadOption.py" >}}
###  **Utilizzo delle opzioni di carico glTF**
Il codice seguente mostra come impostare le opzioni di carico prima di caricare un file glTF.
####  **Capovolgi la Coordinata texture V/T**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-glTFLoadOptions.py" >}}
###  **Utilizzo delle opzioni di carico Ply**
Il codice seguente mostra come impostare le opzioni di carico prima di caricare un modello PLY.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-PlyLoadOptions.py" >}}
###  **Utilizzo delle opzioni di carico DirectX X**
Il codice seguente mostra come impostare le opzioni di carico prima di caricare un file DirectX X.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-XLoadOptions.py" >}}
###  **Utilizza RVM opzioni di carico**
**C#**

```py


import aspose.threed as a3d
# set load options of RVM

scene = a3d.Scene()

opt = a3d.formats.RvmLoadOptions()
opt.cylinder_radial_segments = 32
opt.dish_latitude_segments = 16
opt.dish_longitude_segments = 24
opt.torus_tubular_segments = 40

# import RVM

scene.open("LAD-TOP.rvm", opt);

# save in the OBJ format

scene.save("LAD-TOP.obj", a3d.FileFormat.WAVEFRONT_OBJ);

```

###  **Utilizzo di FBX opzioni di carico**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-FBXLoadOptions.py" >}}
