---
title: Installazione
type: docs
weight: 50
url: /it/java/installation/
description: Aspose ospita tutte le API Java su Aspose Repository. Puoi utilizzare facilmente Aspose.3D per Java API direttamente nei tuoi progetti Maven con configurazioni semplici.
---

## **Installazione di Aspose.3D per Java dal repository Aspose**
Aspose ospita tutte le API Java su [Aspose Repository](https://releases.aspose.com/java/repo/com/aspose/aspose-3d/). È possibile utilizzare facilmente l'API Aspose.3D per Java direttamente nei progetti Maven con configurazioni semplici.

Per prima cosa è necessario specificare la configurazione / posizione del repository Aspose nel file `pom.xml` di Maven come mostrato di seguito:

{{< highlight xml >}}

 <repositories>

    <repository>
        <id>AsposeJavaAPI</id>
        <name>Aspose Java API</name>
        <url>https://releases.aspose.com/java/repo/</url>
    </repository>

</repositories>

{{< /highlight >}}

Quindi definire la dipendenza dell'API Aspose.3D per Java nel `pom.xml` come segue:

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


Se si utilizza JDK‑8, è possibile usare la versione JDK‑8 come segue:

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

Congratulazioni! Hai definito correttamente la dipendenza Maven di Aspose.3D per Java nel tuo progetto Maven.