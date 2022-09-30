---
title: Liste des caractéristiques
type: docs
weight: 30
url: /fr/python-net/feature-list/
---
Aspose.3D Caractéristiques


## **Plateformes supportées**

Les plates-formes Aspose.3D pour Python via .NET peuvent être utilisées sur Windowsx64 ou x86 et une large gamme de distributions Linux avec Python 3.5 ou version ultérieure installée. Il y a des exigences supplémentaires à la plate-forme cible Linux:
- GCC-6 les bibliothèques d'exécution (ou plus tard)
- Dépendances du .NET Core Runtime. L'installation du .NET Core Runtime n'est PAS requise
- Pour Python 3.5-3.7: La construction pymalloc de Python est nécessaire. L'option de build-with-pymalloc Python est activée par défaut. En règle générale, le pymalloc build de Python est marqué avec m suffixe dans le nom de fichier.
- Libpython a partagé la bibliothèque Python. L'option de build-inable-partagé Python est désactivée par défaut, certaines distributions Python ne contiennent pas la bibliothèque partagée libpython. Pour certaines plates-formes Linux, la bibliothèque partagée libpython peut être installée à l'aide du gestionnaire de packages, par exemple: sudo apt-get install libpython3.7. Le problème courant est que la bibliothèque libpython est installée dans un emplacement différent de l'emplacement système standard pour les bibliothèques partagées. Le problème peut être résolu en utilisant les options de construction Python pour définir des chemins de bibliothèque alternatifs lors de la compilation de Python, ou corrigé en créant un lien symbolique vers le fichier de bibliothèque libpython dans l'emplacement standard du système pour les bibliothèques partagées. En règle générale, le nom du fichier de bibliothèque partagé libpythonX.Ym.so.1.0 pour Python 3.5-3.7, ou libpythonX.Y.so.1.0 pour Python 3.8 ou version ultérieure (par exemple: libpython3.7m.so.1.0, libpython3.9.so.1.0).
- Libgdiplus 6.0.1 ou version ultérieure


## **Caractéristique Matrice**

|**Caractéristiques** |` `FBX|` `Collada|` `glTF|` `glTF 2.0|` `U3D|` `PDF|` `STL|` `OBJ|` `PLY|` `3DS|` `ASE|` `X|` `3MF|` `RVM|` `Draco|
|:- |:- |:- |:- |:- |:- |:- |:- |:- |:- |:- |:- |:- |:- |:- |:- |
|` `Lambert Matériel|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>||<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>||<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>||<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>||||
|` ` Matériau Phong|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>||<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>||<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>|||<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>||||
|` `Matériau à base de Shader|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>||<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>|||||||||||||
|` `PBR Matériel||||<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>||||||||||||
|` `PBR Matériau spéculaire||||<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>||||||||||||
|` ` Texture diffuse|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>||<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>||<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>||<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>|||
|` ` Texture avancée|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>||<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>||<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>||||||||
|` ` Mailles polygones|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>||||||<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>||||||<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>||
|` `Mailles à base de triangle|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>|
|` ` Éléments du sommet|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>||<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>|||<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>|
|` ` géométries NURBS|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>|||||||||||||||
|` ` Géométries paramétrées||||||||||||||<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>||
|` ` Transformation locale|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>||||<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>||<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>||
|` `Instancing|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>||||||||||
|` ` Graphique de scène|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>||||<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>||<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>||<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>||
|` ` Propriété personnalisée|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>||<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>||||||||||||
|` ` Squelette|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>||||||||||||||
|` ` Décarteur Morph|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>||||||||||||||
|` ` Animation de la propriété|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>||||||||||||||
|Compression de maille ` `|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>||||<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>|<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>|||||||<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>||<p>![Todo: image_Alt_Texte](accept.png)</p><p> </p>|

