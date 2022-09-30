---
title: Licence
description: "Aspose.3D pour Python via .NET propose différents plans d'achat ou offre un essai gratuit et une licence temporaire de 30 jours pour évaluation en utilisant les politiques de licence et d'abonnement."
type: docs
weight: 80
url: /fr/python-net/licensing/
---
Parfois, pour mieux étudier le système, vous voulez vous plonger dans le code aussi vite que possible. Pour faciliter cela, le Aspose.3D propose différents plans d'achat ou propose un essai gratuit et une licence temporaire de 30 jours pour évaluation.

{{% alert color="primary" %}}

Notez qu'il existe un certain nombre de politiques et de pratiques générales qui vous guident sur la façon d'évaluer, de concéder correctement la licence et d'acheter nos produits. Vous pouvez les trouver dans le["Politiques d'achat et FAQ"](https://purchase.aspose.com/policies)Section.

{{% /alert %}}

## **Évaluer Aspose.3D**
Vous pouvez facilement télécharger Aspose.3D pour l'évaluation. Le paquet d'évaluation est le même que le paquet acheté. La version d'évaluation devient simplement sous licence après avoir ajouté quelques lignes de code pour appliquer la licence.

## **Limitation de la version d'évaluation**
La version d'évaluation fournit toutes les fonctionnalités, sauf ce qui suit:

- Les utilisateurs ne peuvent ouvrir/importer qu'un maximum de 50 3D documents sur une scène.
- Chaque nœud ne peut pas avoir plus de 5 nœuds enfants.
- Chaque nœud ne peut pas avoir plus de 2 entités attachées.
- Chaque géométrie ne peut pas avoir plus de 2 éléments de sommet attachés.
- Chaque nœud ne peut pas avoir plus de 1 matériau.
- Les utilisateurs ne peuvent enregistrer qu'un maximum de 50 3D documents sur une scène.
- Les utilisateurs verront également un filigrane d'évaluation dans les images rendues et tous les autres fichiers de sortie.

{{% alert color="primary" %}} 
Si vous utilisez Aspose.3D sans licence appropriée, il pourrait y déclencher un `aspose.threed.TrialException` lorsque l'utilisation a atteint les restrictions sans licence, vous pouvez désactiver l'exception en:

* [Achetez une licence complète en vedette](https://purchase.aspose.com/buy).
* Demandez une licence temporaire de 30 jours, veuillez vous référer à [Comment obtenir une licence temporaire?](https://purchase.aspose.com/temporary-license) Pour plus d'informations.
* Utilisez manuellement un bloc «essai/excepter» sur «Scène. open/save», cette exception est juste une notification, ignorez que cela n'affectera pas le chargement/sauvegarde de la scène.

{{% /alert %}} 


## **Au sujet de la licence**
Vous pouvez facilement télécharger une version d'évaluation de Aspose.3D pour Python via .NET à partir de son[Page de téléchargement](https://pypi.org/project/aspose.3d/). La version d'évaluation fournit absolument**Les mêmes capacités**Comme la version sous licence de Aspose.3D. De plus, la version d'évaluation devient simplement une licence après avoir acheté une licence et ajouté quelques lignes de code pour appliquer la licence.

La licence est un fichier XML en texte brut qui contient des détails tels que le nom du produit, le nombre de développeurs auxquels il est autorisé, la date d'expiration de l'abonnement, etc. Le fichier est signé numériquement, donc ne modifiez pas le fichier. Même un ajout par inadvertance d'une rupture de ligne supplémentaire au contenu du fichier l'invalidera.

Pour éviter les limitations associées à la version d'évaluation, vous devez définir une licence avant d'utiliser**Aspose.3D**. Vous n'êtes tenu de définir une licence qu'une fois par demande ou par processus.

## Licence achetée

Après l'achat, vous devez appliquer le fichier de licence ou le flux. Cette section décrit les options de la façon dont cela peut être fait, ainsi que des commentaires sur certaines questions courantes.

{{% alert color="primary" %}}

Vous devez définir la licence:
* Une seule fois par domaine d'application
* Avant d'utiliser toute autre Aspose.3D classes

{{% /alert %}}

{{% alert color="primary" %}}

Vous pouvez trouver des informations sur les prix[“Information sur la tarification”](https://purchase.aspose.com/pricing/3d/family)Page.

{{% /alert %}}

### **Définition d'une licence au Aspose.3D pour Python via .NET**

Les licences peuvent être appliquées à partir de divers endroits:

* Chemin explicite
* Le dossier contenant le script python qui appelle Aspose.3D pour Python via .NET
* Stream
* En tant que licence mesurée-un nouveau mécanisme de licence

{{% alert color="primary" %}}

Utilisez la méthode `set_license` pour obtenir une licence pour un composant.

Appeler `set_license` plusieurs fois n'est pas nocif, cela fait juste perdre du temps au processeur.

{{% /alert %}}

Dans les sections ci-dessous, nous allons décrire les deux méthodes courantes utilisées pour définir la licence.

#### **Application d'une licence à l'aide d'un fichier**
La méthode la plus simple pour définir une licence vous oblige à placer le fichier de licence dans le même dossier contenant le script python qui appelle Aspose.3D pour Python et à spécifier simplement le nom du fichier sans son chemin.

Cet extrait de code est utilisé pour définir un fichier de licence:

**Python**

```py
import aspose.threed as a3d

# Instantiate an instance of license and set the license file through its path
license = a3d.License()
license.set_license("Aspose.3D.lic")
```

Lorsque vous appelez la méthode `set_license`, le nom de la licence doit être le même que celui de votre fichier de licence. Par exemple, vous pouvez changer le nom du fichier de licence en "Aspose.3D.lic.xml". Ensuite, dans votre code, vous devez passer le nouveau nom de licence (Aspose.3D.lic xml) à la méthode SetLicense.

#### **Application d'une licence à partir d'un flux**
Vous pouvez charger une licence à partir d'un flux.

Cet extrait de code est utilisé pour appliquer une licence à partir d'un flux:

**Python**

```py
import aspose.threed as a3d

# Instantiate an instance of license and set the license file through its path
license = a3d.License()
license.set_license(stream)
```

#### Appliquer une licence mesurée

Aspose.3D permet aux développeurs d'appliquer une clé mesurée. Il s'agit d'un nouveau mécanisme de licence.

Le nouveau mécanisme de licence sera utilisé avec la méthode de licence existante. Les clients qui souhaitent être facturés en fonction de l'utilisation des fonctionnalités API peuvent utiliser les licences à mesure.

Après avoir terminé toutes les étapes nécessaires pour obtenir ce type de licence, vous recevrez les clés, pas le fichier de licence. Cette clé dosée peut être appliquée à l'aide de la classe `Metered` spécialement introduite à cet effet.

L'exemple de code suivant montre comment définir des clés publiques et privées mestées:

```py
import aspose.threed as a3d

# Create an instance of CAD Metered class
metered = a3d.Metered()

# Access the set_metered_key property and pass public and private keys as parameters
metered.set_metered_key("*****", "*****")

# Get metered data amount before calling API
amountbefore = a3d.metered.get_consumption_quantity()
# Display information
print("Amount Consumed Before: " + str(amountbefore))

# Load the scene from disk.
scene = a3d.Scene.from_file("3D Model.fbx")
# Save as pdf
scene.save("out_pdf.pdf", a3d.FileFormat.PDF)

# Get metered data amount After calling API
amountafter = a3d.metered.get_consumption_quantity()
# Display information
print("Amount Consumed After: " + str(amountafter))
```

{{% alert color="primary" %}}

Veuillez noter que vous devez disposer d'une connexion Internet stable pour une utilisation correcte de la licence Metered, car le mécanisme Metered nécessite une interaction constante avec nos services pour des calculs corrects. Pour plus de détails, reportez-vous à la[«FAQ sur les licences dosées»](https://purchase.aspose.com/faqs/licensing/metered)Section.

{{% /alert %}}



