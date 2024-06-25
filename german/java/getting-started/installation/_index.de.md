---
title: Installation
type: docs
weight: 50
url: /de/java/installation/
description: Aspose hostet alle Java APIs auf Aspose Repository. Sie können Aspose.3D for Java API direkt in Ihren Maven Projekten mit einfachen Konfigurationen verwenden.
---
##  **Installation von Aspose.3D for Java aus Aspose Repository**
Aspose hostet alle Java APIs auf [Aspose Repository](https://releases.aspose.com/java/repo/com/aspose/aspose-3d/). Sie können Aspose.3D for Java API direkt in Ihren Maven Projekten mit einfachen Konfigurationen verwenden.

Zuerst müssen Sie die Aspose Repository-Konfiguration/den Speicherort in Ihrem Maven `pom.xml` wie folgt angeben:

{{< highlight "xml" >}}

 <repositories>

    <repository>
        <id>AsposeJavaAPI</id>
        <name>Aspose Java API</name>
        <url>https://releases.aspose.com/java/repo/</url>
    </repository>

</repositories>

{{< /highlight >}}

Definieren Sie dann Aspose.3D for Java API Abhängigkeit in Ihrem pom.xml wie folgt:

{{< highlight "xml" >}}

 <dependencies>

    <dependency>
        <groupId>com.aspose</groupId>
        <artifactId>aspose-3d</artifactId>
        <version>23.11.0</version>
    </dependency>

</dependencies>

{{< /highlight >}}


Wenn Sie JDK-8 verwenden, können Sie JDK-8 Version wie folgt verwenden:

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

Herzlichen Glückwunsch! Sie haben die Aspose.3D for Java Maven Abhängigkeit in Ihrem Maven Projekt erfolgreich definiert.
