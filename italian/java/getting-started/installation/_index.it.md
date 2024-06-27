---
title: Installation
type: docs
weight: 50
url: /it/java/installation/
description: Aspose ospita tutte le API Java sul repository Aspose. Puoi facilmente utilizzare Aspose.3D for Java API direttamente nei tuoi progetti Maven con semplici configurazioni.
---
##  **Installazione di Aspose.3D for Java da Aspose repository**
Aspose ospita tutte le API Java su [Aspose repository](https://releases.aspose.com/java/repo/com/aspose/aspose-3d/). Puoi facilmente utilizzare Aspose.3D for Java API direttamente nei tuoi progetti Maven con semplici configurazioni.

First you need to specify Aspose Repository configuration / location in your Maven `pom.xml` as below:

{{< highlight "xml" >}}

 <repositories>

    <repository>
        <id>AsposeJavaAPI</id>
        <name>Aspose Java API</name>
        <url>https://releases.aspose.com/java/repo/</url>
    </repository>

</repositories>

{{< /highlight >}}

Quindi definisci Aspose.3D for Java API dipendenza nel tuo pom.xml come segue:

{{< highlight "xml" >}}

 <dependencies>

    <dependency>
        <groupId>com.aspose</groupId>
        <artifactId>aspose-3d</artifactId>
        <version>23.11.0</version>
    </dependency>

</dependencies>

{{< /highlight >}}


Se JDK-8 usi, puoi utilizzare JDK-8 versione come segue:

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

Congratulazioni! Hai definito con successo la dipendenza Aspose.3D for Java Maven nel tuo progetto Maven.
