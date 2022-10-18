﻿---
title: Aspose.3D for Java 20.11 Notes de Libération
type: docs
weight: 6
url: /fr/java/aspose-3d-for-java-20-11-release-notes/
---
{{% alert color="primary" %}}

Cette page contient les notes de publication pour Aspose.3D for Java 20.11.

{{% /alert %}}
## **Améliorations et changements**

|**Clé**|**Résumé**|**Catégorie**|
|:- |:- |:- |
|THREEDNET-747 |Rendre les lignes de bord pour les types CAD dans le moteur de rendu Web.|Correction de bogue|
|THREEDNET-748 |Améliorer l'éclairage dans le rendu Web|Correction de bogue|
|THREEDNET-755 |Attributs de modèle non pris en charge dans certains fichiers FBX 6.1.|Correction de bogue|
|THREEDNET-757 |PLY fichier avec la propriété int64 ne sont pas pris en charge.|Correction de bogue|
|THREEDNET-756 |3MF fichier exporté en utilisant la dernière norme ne peut pas être ouvert.|Correction de bogue|
|THREEDNET-758 |Le fichier FBX 6.0 ne peut pas être importé.|Correction de bogue|
|THREEDNET-760 |Améliorer la compatibilité des fichiers ASE|Correction de bogue|
|THREEDNET-761 |Autoriser spécifier l'encodage pour les fichiers 3D basés sur le texte.|Amélioration|
|THREEDNET-762 |Exportez la scène au HTML en utilisant notre dernier moteur de rendu.|Nouvelle fonctionnalité|
|THREEDNET-763 |Ajoutez le soutien de la collada non standard exportée par l'exportateur inconnu.|Amélioration|
|THREEDNET-765 |Optimiser les performances de chargement du fichier binaire PLY|Améliorer|
|THREEDNET-768 |Le fichier binaire STL exporté par Rhinocéros ne peut pas être importé.|Correction de bogue|
|THREEDNET-769 |Ajouter le soutien des relations en FBX 6.0|Correction de bogue|
|TRHEEDNET-770 |Un caractère d'échappement incorrect dans le fichier FBX entraînera l'échec de l'importation du Aspose.3D.|Correction de bogue|
|THREEDNET-771 |Ajouter une prise en charge des données d'intégration dans FBX|Correction de bogue|


## API changements ##


Le changement majeur dans cette version est que le fichier HTML5 exporté n'utilisera plus l'ancien moteur de rendu.

Au lieu de cela, un moteur de rendu basé sur WebAssembly est utilisé pour le rendu.

Beaucoup de bug ont été corrigés dans cette version.

### Ajout d'une nouvelle propriété à la classe com.aspose.threed.VertexElementUserData:

{{< highlight "java" >}}

    /**
     * Gets the indices data
     */
    @Override
    public List<Integer> getIndices();

{{< /highlight >}}

Cette propriété est ajoutée afin que les fichiers fbx contiennent des données utilisateur mises en accusation puissent être correctement importées.


### Ajout d'une nouvelle propriété à la classe com.aspose.threed.IOConfig:

{{< highlight "java" >}}

    /**
     * Gets the default encoding for text-based files.
     * Default value is null which means the importer/exporter will decide which encoding to use.
     */
    public Charset getEncoding();
    
    /**
     * Sets the default encoding for text-based files.
     * Default value is null which means the importer/exporter will decide which encoding to use.
     * @param value New value
     */
    public void setEncoding(Charset value);

{{< /highlight >}}

Ceci est utilisé pour remplacer l'encodage interne par défaut lors de l'importation/exportation, de sorte que vous pouvez contrôler manuellement l'encodage des formats basés sur du texte.