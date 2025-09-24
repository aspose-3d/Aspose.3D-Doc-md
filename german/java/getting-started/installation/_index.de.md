---
title: Installation
type: docs
weight: 50
url: /de/java/installation/
description: "Aspose hostet alle Java-APIs im Aspose Repository. Sie können Aspose.3D for Java API direkt in Ihren Maven-Projekten mit einfachen Konfigurationen verwenden."
---

## **Installation von Aspose.3D für Java aus dem Aspose Repository**
Aspose hostet alle Java‑APIs im [Aspose Repository](https://releases.aspose.com/java/repo/com/aspose/aspose-3d/). Sie können Aspose.3D für Java API direkt in Ihren Maven‑Projekten mit einfachen Konfigurationen verwenden.

Zuerst müssen Sie die Aspose‑Repository‑Konfiguration / den Speicherort in Ihrer Maven‑`pom.xml` wie folgt angeben:

{{< highlight xml >}}

 <repositories>

    <repository>
        <id>AsposeJavaAPI</id>
        <name>Aspose Java API</name>
        <url>https://releases.aspose.com/java/repo/</url>
    </repository>

</repositories>

{{< /highlight >}}

Definieren Sie dann die Aspose.3D für Java‑API‑Abhängigkeit in Ihrer `pom.xml` wie folgt:

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


Wenn Sie JDK‑8 verwenden, können Sie die JDK‑8‑Version wie folgt nutzen:

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

Herzlichen Glückwunsch! Sie haben die Aspose.3D für Java Maven‑Abhängigkeit erfolgreich in Ihrem Maven‑Projekt definiert.