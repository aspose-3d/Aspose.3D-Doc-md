---
title: Installation
type: docs
weight: 50
url: /fr/java/installation/
description: Aspose héberge toutes les API Java sur le référentiel Aspose. Vous pouvez facilement utiliser Aspose.3D for Java API directement dans vos projets Maven avec des configurations simples.
---
##  **Installation de Aspose.3D for Java à partir du référentiel Aspose**
Aspose héberge toutes les API Java sur [Aspose Référentiel](https://releases.aspose.com/java/repo/com/aspose/aspose-3d/). Vous pouvez facilement utiliser Aspose.3D for Java API directement dans vos projets Maven avec des configurations simples.

Vous devez d'abord spécifier la configuration/l'emplacement du dépôt Aspose dans votre Maven `pom.xml` comme ci-dessous:

{{< highlight "xml" >}}

 <repositories>

    <repository>
        <id>AsposeJavaAPI</id>
        <name>Aspose Java API</name>
        <url>https://releases.aspose.com/java/repo/</url>
    </repository>

</repositories>

{{< /highlight >}}

Définissez ensuite la dépendance Aspose.3D for Java API dans votre pom.xml comme suit:

{{< highlight "xml" >}}

 <dependencies>

    <dependency>
        <groupId>com.aspose</groupId>
        <artifactId>aspose-3d</artifactId>
        <version>23.11.0</version>
    </dependency>

</dependencies>

{{< /highlight >}}


Si vous utilisez JDK-8, vous pouvez utiliser JDK-8 version comme suit:

{{< highlight "xml" >}}

 <dependencies>

    <dependency>
        <groupId>com.aspose</groupId>
        <artifactId>aspose-3d</artifactId>
        <version>23.11.0</version>
        <classifier>jdk8</classifier>
    </dependency>

</dependencies>

{{< /highlight >}}

Félicitations! Vous avez défini avec succès la dépendance Aspose.3D for Java Maven dans votre projet Maven.
