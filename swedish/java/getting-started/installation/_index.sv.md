---
title: Installation
type: docs
weight: 50
url: /sv/java/installation/
description: Aspose är värd för alla Java API på Aspose arkiv. Du kan enkelt använda Aspose.3D for Java API direkt i dina Maven-projekt med enkla inställningar.
---
##  **Installerar Aspose.3D for Java från Aspose arkiv**
Aspose värd för alla Java API på [Aspose Arkiv](https://releases.aspose.com/java/repo/com/aspose/aspose-3d/). Du kan enkelt använda Aspose.3D for Java API direkt i dina Maven-projekt med enkla inställningar.

Först måste du ange Aspose Arkivets inställning / plats i Maven `pom.xml` som nedan:

{{< highlight "xml" >}}

 <repositories>

    <repository>
        <id>AsposeJavaAPI</id>
        <name>Aspose Java API</name>
        <url>https://releases.aspose.com/java/repo/</url>
    </repository>

</repositories>

{{< /highlight >}}

Ange sedan Aspose.3D for Java API beroende i din pom.xml på följande sätt:

{{< highlight "xml" >}}

 <dependencies>

    <dependency>
        <groupId>com.aspose</groupId>
        <artifactId>aspose-3d</artifactId>
        <version>23.11.0</version>
    </dependency>

</dependencies>

{{< /highlight >}}


Om du använder JDK-8 kan du använda JDK-8-versionen enligt följande:

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

Grattis! Du har definierat Aspose.3D for Java Maven i ditt Maven-projekt med framgång.
