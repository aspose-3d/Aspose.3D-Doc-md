---
title: Licence
type: docs
weight: 60
url: /fr/java/licensing/
description: Vous pouvez facilement télécharger/installer Aspose.3D for Java à partir du dépôt Aspose pour l'évaluation. Le téléchargement d'évaluation est le même que le téléchargement acheté. La version d'évaluation devient simplement sous licence lorsque vous ajoutez quelques lignes de code pour appliquer la licence.
---
## **Évaluer Aspose.3D**
Vous pouvez facilement télécharger/installer Aspose.3D for Java à partir de[Référentiel Aspose](https://releases.aspose.com/java/repo/com/aspose/aspose-3d/)Pour l'évaluation. Le téléchargement d'évaluation est le même que le téléchargement acheté. La version d'évaluation devient simplement sous licence lorsque vous ajoutez quelques lignes de code pour appliquer la licence.

La version d'évaluation fournit toutes les fonctionnalités, sauf ce qui suit:

- Les utilisateurs ne peuvent ouvrir/importer qu'un maximum de 50 3D documents sur une scène.
- Les utilisateurs ne peuvent enregistrer qu'un maximum de 50 3D documents sur une scène.
- Les utilisateurs verront également un filigrane d'évaluation dans les images rendues et tous les autres fichiers de sortie.
- Chaque nœud ne peut pas avoir plus de 5 nœuds enfants.
- Chaque nœud ne peut pas avoir plus de 2 entités attachées.
- Chaque géométrie ne peut pas avoir plus de 2 éléments de sommet attachés.
- Chaque nœud ne peut pas avoir plus de 1 matériau.

{{% alert color="primary" %}} 

Si vous utilisez Aspose.3D sans une licence appropriée, il pourrait déclencher un**Com. aspose. trois. TrialException**Lorsque l'utilisation a atteint les restrictions sans licence, vous pouvez désactiver l'exception en:

* [Achetez une licence complète en vedette](https://purchase.aspose.com/buy).
* Demandez une licence temporaire de 30 jours, veuillez vous référer à [Comment obtenir une licence temporaire?](https://purchase.aspose.com/temporary-license) Pour plus d'informations.
.
* Appelez 'com.aspose.threed.TrialException.setSuppressTrialException(true)'avant vos méthodes 'open'/'sauvegarde', le 'TrialException' ne sera pas soulevé lors de l'appel 'ouvre'/'sauvegarde' sur Scène, mais les restrictions ci-dessus ne seront pas levées.
* Utilisez manuellement un bloc «essayer/catch» sur «Scène. open/save», cette exception est juste une notification, ignorez que cela n'affectera pas le chargement/sauvegarde de la scène.

{{% /alert %}} 
## **Application d'une licence**
La licence est un fichier XML en texte brut qui contient des détails tels que le nom du produit, le nombre de développeurs auxquels il est autorisé, la date d'expiration de l'abonnement, etc. Le fichier est signé numériquement, alors ne modifiez pas le fichier; même l'ajout par inadvertance d'une rupture de ligne supplémentaire dans le fichier l'invalidera. Vous devez définir une licence avant d'effectuer des opérations avec des documents. Assurez-vous de le faire avant de créer un objet Scène.

Les licences peuvent être appliquées à partir de divers endroits:

- Chemin explicite
- Le dossier qui contient le fichier JAR du 076104881.
- Une ressource intégrée dans le JAR qui a appelé Aspose.3D JAR.

Utilisez la méthode `License.setLicense` pour obtenir une licence pour les API. Souvent, le moyen le plus simple de définir une licence est de placer le fichier de licence dans le même dossier que le JAR de Aspose.3D et de spécifier simplement le nom de fichier sans chemin.
### **Appliquer la licence à l'aide d'un objet Fichier ou Stream**
Dans cet exemple, Aspose.3D tentera de trouver le fichier de licence dans le dossier qui contient les JAR de votre application.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-license-ApplyLicenseUsingFile.java" >}}

Initialise une licence à partir d'un flux.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-license-ApplyLicenseUsingStreamObject.java" >}}
### **Y compris le fichier de licence en tant que ressource intégrée**
Vous pouvez simplement copier le fichier LIC dans le dossier `resources` de votre projet. La reconstruction du projet devrait intégrer le. Fichier lic dans l'application. Fichier pot. Après cela, vous pouvez appliquer la licence en utilisant le code comme ci-dessous:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-license-FileAsEmbeddedResource.java" >}}
### **Valider la licence**
Il est possible de valider si la licence a été réglée correctement ou non. La classe de licence a le champ isLicensed qui retournera vrai si la licence a été correctement définie.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-license-ValidateLicense.java" >}}
## **Appliquer une licence mesurée**
Aspose.3D permet aux développeurs d'appliquer la clé mesurée. C'est un nouveau mécanisme de licence. Le nouveau mécanisme de licence sera utilisé avec la méthode de licence existante. Les clients qui souhaitent être facturés en fonction de l'utilisation des fonctionnalités API peuvent utiliser la licence mesurée. Pour plus de détails, veuillez vous référer à[FAQ sur les licences dosées](https://purchase.aspose.com/faqs/licensing/metered)Section.

Une nouvelle classe `Metered` a été introduite pour appliquer la clé mesurée. Voici l'exemple de code montrant comment définir la clé publique et privée mesurée.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-license-PublicAndPrivateKeys.java" >}}
## **Quand appliquer une licence**
Suivez ces règles simples:

- La licence ne doit être définie qu'une seule fois par domaine d'application.
- Vous devez définir la licence avant d'utiliser toute autre classe Aspose.3D.
- Appeler License.SetLicense plusieurs fois n'est pas nocif, mais fait perdre du temps au processeur.

Si vous développez une bibliothèque de classes, vous pouvez appeler Licence. SetLicense à partir d'un constructeur statique de votre classe qui utilise Aspose.3D. Le constructeur statique s'exécute avant qu'une instance de votre classe ne soit créée en vous assurant que la licence Aspose.3D est correctement définie.
## **Vous pouvez changer le nom du fichier de licence**
Le nom du fichier de licence ne doit pas être «Aspose.3D.LIC». Vous pouvez le renommer en quelque chose que vous aimez et utiliser ce nom lorsque vous appelez Licence. SetLicense.
## **Exception Ne trouve pas le nom de fichier de licence**
Lorsque vous achetez et téléchargez une licence, le site Web Aspose nomme le fichier de licence `Aspose.3D.LIC`. Vous téléchargez le fichier de licence à l'aide de votre navigateur. Certains navigateurs reconnaissent le fichier de licence comme XML et apposent un. Extension xml de sorte que le nom complet du fichier sur votre ordinateur devient `Aspose.3D.lic.XML`.

Lorsque le Microsoft Windows, par exemple, est configuré pour masquer les extensions de types de fichiers connus (malheureusement, c'est par défaut dans la plupart des installations Windows), le fichier de licence vous apparaîtra comme `Aspose.3D.LIC` dans l'explorateur Windows. Vous êtes susceptible de penser que c'est le vrai nom de fichier et appeler Licence. SetLicence passant `Aspose.3D.LIC`, mais il n'y a pas de tel fichier, d'où l'exception.

Afin de résoudre le problème, renommez le fichier pour supprimer l'invisible. Extension xml. Nous vous recommandons également de désactiver l'option "cacher les extensions" dans Microsoft Windows.

## **Utilisation de plusieurs API à partir de Aspose**
Si vous utilisez plusieurs API Aspose dans votre application, par exemple Aspose.3D et Aspose.Cells, voici quelques conseils utiles.

- Définissez la licence pour chaque Aspose API séparément. Même si vous avez un seul fichier de licence pour toutes les API, par exemple `Aspose.Total.lic`, vous devez toujours appeler le `License.setLicense` séparément pour chaque Aspose API que vous utilisez dans votre application.
- Utilisez le nom de classe de licence entièrement qualifié. Chaque Aspose API a une classe de licence dans son espace de noms. Par exemple, Aspose.3D a `com.aspose.3d.License` et Aspose.Cells a `com.aspose.cells.License` classe. L'utilisation du nom de classe entièrement qualifié vous permet d'éviter toute confusion quant à la licence appliquée à quel produit.
