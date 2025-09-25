---
title: Installation
type: docs
weight: 50
url: /fr/java/installation/
description: Aspose héberge toutes les API Java sur le dépôt Aspose. Vous pouvez facilement utiliser Aspose.3D for Java API directement dans vos projets Maven avec des configurations simples.
---

## **Installation d'Aspose.3D pour Java depuis le référentiel Aspose**

Aspose héberge toutes les API Java sur le [Aspose Repository](https://releases.aspose.com/java/repo/com/aspose/aspose-3d/). Vous pouvez facilement utiliser l'API Aspose.3D pour Java directement dans vos projets Maven avec des configurations simples.

Tout d'abord, vous devez spécifier la configuration / l'emplacement du référentiel Aspose dans votre Maven `pom.xml` comme indiqué ci-dessous :

{{< highlight xml >}}
 <repositories>

    <repository>
        <id>AsposeJavaAPI</id>
        <name>Aspose Java API</name>
        <url>https://releases.aspose.com/java/repo/</url>
    </repository>

</repositories>
{{< /highlight >}}

Ensuite, définissez la dépendance de l'API Aspose.3D pour Java dans votre `pom.xml` comme suit :

{{< highlight xml >}}
 <dependencies>

    <dependency>
        <groupId>com.aspose</groupId>
        <artifactId>aspose-3d</artifactId>
        <version>25.9.0</version>
    </dependency>
    <dependency>
      <groupId>org.bouncycastle</groupId>
      <artifactId>bc-fips</artifactId>
      <version>2.1.1</version>
    </dependency>


    <dependency>
      <groupId>org.lwjgl</groupId>
      <artifactId>lwjgl</artifactId>
      <version>${lwjgl.version}</version>
    </dependency>
      <artifactId>lwjgl-platform</artifactId>
      <version>${lwjgl.version}</version>
      <classifier>natives-windows</classifier>
    <dependency>
      <groupId>org.lwjgl</groupId>
      <artifactId>lwjgl-vulkan</artifactId>
      <version>${lwjgl.version}</version>
    </dependency>
</dependencies>
{{< /highlight >}}

Si vous utilisez JDK-8, vous pouvez utiliser la version JDK-8 comme suit :

{{< highlight xml >}}
 <dependencies>

    <dependency>
        <groupId>com.aspose</groupId>
        <artifactId>aspose-3d</artifactId>
        <version>25.9.0</version>
        <classifier>jdk8</classifier>
    </dependency>
    <dependency>
      <groupId>org.bouncycastle</groupId>
      <artifactId>bc-fips</artifactId>
      <version>2.1.1</version>
    </dependency>
</dependencies>
{{< /highlight >}}

Félicitations ! Vous avez défini avec succès la dépendance Maven Aspose.3D pour Java dans votre projet Maven.