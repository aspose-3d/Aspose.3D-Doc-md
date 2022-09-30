---
title: Installation
type: docs
weight: 50
url: /fr/java/installation/
description: Aspose héberge toutes les API Java sur le référentiel Aspose. Vous pouvez facilement utiliser Aspose.3D for Java API directement dans vos projets Maven avec des configurations simples.
---
## **Installation du Aspose.3D for Java à partir du dépôt Aspose**
Aspose héberge toutes les API Java sur[Référentiel Aspose](https://repository.aspose.com/webapp/#/artifacts/browse/tree/General/repo/com/aspose/aspose-3d). Vous pouvez facilement utiliser Aspose.3D for Java API directement dans vos projets Maven avec des configurations simples.

Tout d'abord, vous devez spécifier Aspose Configuration/emplacement du référentiel dans votre Maven `pom.xml` comme ci-dessous:

{{< highlight "java" >}}

 <repositories>

    <repository>
        <id>AsposeJavaAPI</id>
        <name>Aspose Java API</name>
        <url>http://repository.aspose.com/repo/</url>
    </repository>

</repositories>

{{< /highlight >}}

Définissez ensuite la dépendance Aspose.3D for Java API dans votre pom.xml comme suit:

{{< highlight "java" >}}

 <dependencies>

    <dependency>
        <groupId>com.aspose</groupId>
        <artifactId>aspose-3d</artifactId>
        <version>21.4</version>
    </dependency>

</dependencies>

{{< /highlight >}}

Félicitations! Vous avez défini avec succès la dépendance Aspose.3D for Java Maven dans votre projet Maven.
