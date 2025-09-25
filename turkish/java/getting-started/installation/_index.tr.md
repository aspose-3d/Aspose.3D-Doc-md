---
title: Kurulum
type: docs
weight: 50
url: /tr/java/installation/
description: "Aspose, tüm Java API'lerini Aspose Repository'de barındırır. Maven projelerinizde basit yapılandırmalarla Aspose.3D for Java API'yi doğrudan kolayca kullanabilirsiniz."
---

## **Aspose Repository'den Aspose.3D for Java'ı Kurma**
Aspose, tüm Java API'lerini Aspose Repository'de barındırır. Basit yapılandırmalarla Aspose.3D for Java API'sını Maven projelerinizde doğrudan kolayca kullanabilirsiniz.

İlk olarak, Maven `pom.xml` dosyanızda Aspose Repository yapılandırmasını / konumunu aşağıdaki gibi belirtmeniz gerekir:

{{< highlight xml >}}
 <repositories>

    <repository>
        <id>AsposeJavaAPI</id>
        <name>Aspose Java API</name>
        <url>https://releases.aspose.com/java/repo/</url>
    </repository>

</repositories>
{{< /highlight >}}

Ardından, pom.xml dosyanızda Aspose.3D for Java API bağımlılığını aşağıdaki gibi tanımlayın:

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

JDK-8 kullanıyorsanız, JDK-8 sürümünü aşağıdaki gibi kullanabilirsiniz:

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

Tebrikler! Maven projenizde Aspose.3D for Java Maven bağımlılığını başarıyla tanımladınız.