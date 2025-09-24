---
title: Установка
type: docs
weight: 50
url: /ru/java/installation/
description: Aspose размещает все Java API в репозитории Aspose. Вы можете легко использовать Aspose.3D for Java API напрямую в ваших Maven‑проектах с простыми настройками.
---

## **Установка Aspose.3D for Java из репозитория Aspose**
Aspose размещает все Java API в [Aspose Repository](https://releases.aspose.com/java/repo/com/aspose/aspose-3d/). Вы можете легко использовать Aspose.3D for Java API напрямую в своих Maven‑проектах, задав простые конфигурации.

Сначала необходимо указать конфигурацию / расположение Aspose Repository в вашем Maven‑файле `pom.xml`, как показано ниже:

{{< highlight xml >}}
<repositories>
    <repository>
        <id>AsposeJavaAPI</id>
        <name>Aspose Java API</name>
        <url>https://releases.aspose.com/java/repo/</url>
    </repository>
</repositories>
{{< /highlight >}}

Затем определите зависимость Aspose.3D for Java API в вашем `pom.xml` следующим образом:

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

Если вы используете JDK‑8, можно задать версию для JDK‑8 следующим образом:

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

Поздравляем! Вы успешно добавили зависимость Aspose.3D for Java в ваш Maven‑проект.