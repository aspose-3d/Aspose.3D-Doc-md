---
title: Comment exécuter Aspose.3D for Java dans Docker
type: docs
description: Exécutez Aspose.3D for Java dans un conteneur Docker pour Linux.
weight: 139
url: /fr/java/how-to-run-aspose-3d-in-docker/
---
Les microservices, associés à la conteneurisation, permettent de combiner facilement les technologies. Docker vous permet d'intégrer facilement la fonctionnalité Aspose.3D dans votre application, quelle que soit la technologie de votre pile de développement.

Dans le cas où vous ciblez des microservices, ou si la technologie principale de votre pile n'est pas .NET, C++ ou Java, mais vous avez besoin de Aspose.3D, ou si vous utilisez déjà Docker dans votre pile, vous pouvez être intéressé par l'utilisation de Aspose.3D for Java dans un conteneur Docker.

## Prérequis

- Docker doit être installé sur votre système.

## Créer une application Java

Dans cet exemple, vous créez une application Java qui crée un simple fichier 3d, l'enregistre et le lit. L'application peut ensuite être construite et exécutée dans Docker.

### Création de l'application Java

Créez une application Java dans Eclipse en utilisant le code suivant. Dans cet exemple, nous utilisons Aspose.3D for Java pour créer un plan dans la scène 3D et définir le vecteur, puis l'enregistrer au format obj.

{{< highlight "java" >}}
// For complete examples and data files, please go to https://github.com/aspose-3d/Aspose.3D-for-Java
// The path to the documents directory.
String MyDir = RunExamples.getDataDir();
// Initialize Scene
Scene scene = new Scene();
// Initialize Plane
Plane plane = new Plane();
// Set Vector
plane.setUp(new Vector3(1, 1, 3));
scene.getRootNode().createChildNode(plane);
//This will generate a plane that has customized orientation
scene.save(MyDir+"ChangePlaneOrientation.obj", FileFormat.WAVEFRONTOBJ);

{{< /highlight >}}

### Faire l'application Java dans un paquet jar

La figure suivante montre un moyen de créer un paquet jar en utilisant le menu "Exporter" dans Eclipse.

**! [Faire Jar en utilisant Eclipse](MakeJar.png)**

Maintenant que nous avons écrit un programme Java en utilisant Aspose.3D for Java, nous avons obtenu un paquet jar. Ensuite, nous allons faire un dockerfile.

### Configuration d'un fichier Dockerfile

L'étape suivante consiste à créer et configurer le fichier Dockerfile.

1. Créez le fichier Dockerfile et placez-le à côté du paquet jar. Conservez ce nom de fichier sans extension (valeur par défaut).
2. Dans le fichier Dockerfile, spécifiez:

{{< highlight "plain" >}}
   FROM williamyeh/java8:latest

   VOLUME /tmp

   ADD TestDocker.jar app.jar

   ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom","-jar","/app.jar"]
{{< /highlight >}}

### Création et exécution de l'application dans Docker

Maintenant, l'application peut être construite et exécutée dans Docker. Ouvrez votre invite de commande préférée, changez de répertoire dans le dossier contenant le fichier Dockerfile et exécutez la commande suivante:

{{< highlight "plain" >}}
docker build -t java-app .
{{< /highlight >}}

Après avoir exécuté la commande ci-dessus, vous obtiendrez la sortie du fichier 3D. À ce stade, un programme Java a été exécuté avec succès dans Linux Docker.
