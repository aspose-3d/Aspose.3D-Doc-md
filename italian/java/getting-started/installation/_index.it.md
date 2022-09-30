---
title: Installazione
type: docs
weight: 50
url: /it/java/installation/
description: Aspose ospita tutte le API Java sul repository Aspose. Puoi facilmente utilizzare Aspose.3D for Java API direttamente nei tuoi progetti Maven con semplici configurazioni.
---
## **Installazione di Aspose.3D for Java dal repository Aspose**
Aspose ospita tutte le API Java su[Aspose Repository](https://repository.aspose.com/webapp/#/artifacts/browse/tree/General/repo/com/aspose/aspose-3d). Puoi facilmente utilizzare Aspose.3D for Java API direttamente nei tuoi progetti Maven con semplici configurazioni.

Per prima cosa devi specificare la configurazione/posizione del repository Maven `pom.xml` come di seguito:

{{< highlight "java" >}}

 <repositories>

    <repository>
        <id>AsposeJavaAPI</id>
        <name>Aspose Java API</name>
        <url>http://repository.aspose.com/repo/</url>
    </repository>

</repositories>

{{< /highlight >}}

Quindi definisci la dipendenza Aspose.3D for Java API nel tuo pom.xml come segue:

{{< highlight "java" >}}

 <dependencies>

    <dependency>
        <groupId>com.aspose</groupId>
        <artifactId>aspose-3d</artifactId>
        <version>21.4</version>
    </dependency>

</dependencies>

{{< /highlight >}}

Congratulazioni! Hai definito con successo la dipendenza Aspose.3D for Java Maven nel tuo progetto Maven.
