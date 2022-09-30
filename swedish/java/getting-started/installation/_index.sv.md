---
title: Anläggning
type: docs
weight: 50
url: /sv/java/installation/
description: Aspose värd alla Java APIs på Aspose arkiv. Du kan enkelt använda Aspose.3D for Java API direkt i dina Maven projekt med enkel konfiguration iii).
---
## **Installera Aspose.3D for Java från Aspose Arkiv**
Aspose värd för alla Java APIs[Aspose Arkiv](https://repository.aspose.com/webapp/#/artifacts/browse/tree/General/repo/com/aspose/aspose-3d). Du kan enkelt använda Aspose.3D for Java API direkt i dina Maven projekt med enkel konfiguration iii).

Först måste du ange Aspose arkivkonfiguration / plats i din Maven `pom.xml` enligt nedan:

{{< highlight "java" >}}

 <repositories>

    <repository>
        <id>AsposeJavaAPI</id>
        <name>Aspose Java API</name>
        <url>http://repository.aspose.com/repo/</url>
    </repository>

</repositories>

{{< /highlight >}}

Definiera sedan Aspose.3D for Java API beroende i din pom.xml enligt följande:

{{< highlight "java" >}}

 <dependencies>

    <dependency>
        <groupId>com.aspose</groupId>
        <artifactId>aspose-3d</artifactId>
        <version>21.4</version>
    </dependency>

</dependencies>

{{< /highlight >}}

Grattis! Du har framgångsrikt definierat beroendet Aspose.3D for Java i ditt projekt Maven.
