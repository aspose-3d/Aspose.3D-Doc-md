---
title: Installation
type: docs
weight: 50
url: /sv/java/installation/
description: "Aspose hostar alla Java‑API:er på Aspose Repository. Du kan enkelt använda Aspose.3D for Java API direkt i dina Maven‑projekt med enkla konfigurationer."
---

## **Installera Aspose.3D för Java från Aspose Repository**
Aspose är värd för alla Java‑API:er på [Aspose Repository](https://releases.aspose.com/java/repo/com/aspose/aspose-3d/). Du kan enkelt använda Aspose.3D för Java‑API direkt i dina Maven‑projekt med enkla konfigurationer.

Först måste du ange Aspose Repository‑konfigurationen / platsen i din Maven `pom.xml` som nedan:

{{< highlight xml >}}

 <repositories>

    <repository>
        <id>AsposeJavaAPI</id>
        <name>Aspose Java API</name>
        <url>https://releases.aspose.com/java/repo/</url>
    </repository>

</repositories>

{{< /highlight >}}

Definiera sedan Aspose.3D för Java‑API‑beroendet i din pom.xml på följande sätt:

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

Om du använder JDK‑8 kan du använda JDK‑8‑versionen enligt följande:

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

Grattis! Du har framgångsrikt definierat Aspose.3D för Java Maven‑beroendet i ditt Maven‑projekt.