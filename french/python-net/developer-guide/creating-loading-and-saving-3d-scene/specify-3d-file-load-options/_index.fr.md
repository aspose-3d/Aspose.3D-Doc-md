---
title: Spécifiez 3D Options de chargement de fichier
type: docs
weight: 30
url: /fr/python-net/specify-3d-file-load-options/
description: Il existe plusieurs surcharges de méthode Scene.Open ou surcharges de constructeur de classe Scène qui acceptent un objet LoadOptions. Chaque format de charge a une classe correspondante qui contient les options de charge pour ce format de charge.
---
##  **3D Options de chargement des fichiers**
Il existe plusieurs surcharges de méthode [`Scene.open`](https://reference.aspose.com/3d/net/aspose.threed/scene) ou surcharges de constructeur de classe Scene qui acceptent un objet `LoadOptions`. Cela devrait être un objet d'une classe dérivée de la classe `LoadOptions`. Chaque format de chargement a une classe correspondante qui contient des options de chargement pour ce format de chargement, par exemple il y a `ColladaSaveOptions` pour le format de sauvegarde `FileFormat.Collada`.
###  **Utilisation des options de chargement de 3DS discret**
Le code ci-dessous montre comment définir les options de chargement avant de charger un fichier Discreet 3DS.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-Discreet3DSOption.py" >}}
###  **Utilisation des options de charge Obj**
Le code ci-dessous montre comment définir les options de chargement avant de charger un fichier 3D Obj.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-ObjLoadOption.py" >}}
###  **Utilisation des options de chargement STL**
Le code ci-dessous montre comment définir les options de chargement avant de charger un fichier STL.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-STLLoadOption.py" >}}
###  **Utilisation des options de chargement U3D**
Le code ci-dessous montre comment définir les options de chargement avant de charger un fichier U3D.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-U3DLoadOption.py" >}}
###  **Utilisation des options de chargement glTF**
Le code ci-dessous montre comment définir les options de chargement avant de charger un fichier glTF.
####  **Retournez la coordination de la texture V/T**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-glTFLoadOptions.py" >}}
###  **Utilisation des options de charge Ply**
Le code ci-dessous montre comment définir les options de chargement avant de charger un modèle PLY.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-PlyLoadOptions.py" >}}
###  **Utilisation des options de charge DirectX X**
Le code ci-dessous montre comment définir les options de chargement avant de charger un fichier DirectX X.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-XLoadOptions.py" >}}
###  **Utiliser les options de chargement RVM**
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

###  **Utilisation des options de chargement FBX**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-FBXLoadOptions.py" >}}
