---
title: Installation
type: docs
weight: 50
url: /de/java/installation/
description: Aspose hostet alle Java APIs auf Aspose Repository. Sie können Aspose.3D for Java API direkt in Ihren Projekten Maven mit einfachen Konfigurationen verwenden.
---
## **Installation Aspose.3D for Java von Aspose Repository**
Aspose hostet alle Java APIs auf[Aspose Repository](https://repository.aspose.com/webapp/#/artifacts/browse/tree/General/repo/com/aspose/aspose-3d). Sie können Aspose.3D for Java API direkt in Ihren Projekten Maven mit einfachen Konfigurationen verwenden.

Zuerst müssen Sie Aspose Repository-Konfiguration/Standort in Ihrer Maven `pom.xml` wie folgt angeben:

{{< highlight "java" >}}

 <repositories>

    <repository>
        <id>AsposeJavaAPI</id>
        <name>Aspose Java API</name>
        <url>http://repository.aspose.com/repo/</url>
    </repository>

</repositories>

{{< /highlight >}}

Definieren Sie dann Aspose.3D for Java API Abhängigkeit in Ihrem pom.xml wie folgt:

{{< highlight "java" >}}

 <dependencies>

    <dependency>
        <groupId>com.aspose</groupId>
        <artifactId>aspose-3d</artifactId>
        <version>21.4</version>
    </dependency>

</dependencies>

{{< /highlight >}}

Herzlichen Glückwunsch! Sie haben die Aspose.3D for Java Maven Abhängigkeit in Ihrem Maven-Projekt erfolgreich definiert.
