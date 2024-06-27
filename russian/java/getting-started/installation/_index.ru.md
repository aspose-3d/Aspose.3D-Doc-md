---
title: Installation
type: docs
weight: 50
url: /ru/java/installation/
description: Aspose размещает все API Java в репозитории Aspose. Вы можете легко использовать Aspose.3D for Java API непосредственно в ваших проектах Maven с простыми конфигурациями.
---
##  **Установка Aspose.3D for Java из репозитория Aspose**
Aspose размещает все API Java на [Репозиторий Aspose](https://releases.aspose.com/java/repo/com/aspose/aspose-3d/). Вы можете легко использовать Aspose.3D for Java API непосредственно в ваших проектах Maven с простыми конфигурациями.

Сначала вам нужно указать конфигурацию/расположение репозитория Aspose в вашем Maven `pom.xml`, как показано ниже:

{{< highlight "xml" >}}

 <repositories>

    <repository>
        <id>AsposeJavaAPI</id>
        <name>Aspose Java API</name>
        <url>https://releases.aspose.com/java/repo/</url>
    </repository>

</repositories>

{{< /highlight >}}

Затем определите зависимость Aspose.3D for Java API в вашем pom.xml следующим образом:

{{< highlight "xml" >}}

 <dependencies>

    <dependency>
        <groupId>com.aspose</groupId>
        <artifactId>aspose-3d</artifactId>
        <version>23.11.0</version>
    </dependency>

</dependencies>

{{< /highlight >}}


Если вы используете JDK-8, вы можете использовать JDK-8 версию следующим образом:

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

Поздравляем! Вы успешно определили зависимость Aspose.3D for Java Maven в вашем проекте Maven.
