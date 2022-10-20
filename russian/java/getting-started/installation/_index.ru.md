---
title: Установка
type: docs
weight: 50
url: /ru/java/installation/
description: Aspose размещает все API Java в Репозитории Aspose. Вы можете легко использовать Aspose.3D for Java API непосредственно в ваших проектах Maven с простыми конфигурациями.
---
## **Установка Aspose.3D for Java из Репозитория Aspose**
Aspose размещает все API Java на[Aspose Репозиторий](https://releases.aspose.com/java/repo/com/aspose/aspose-3d/). Вы можете легко использовать Aspose.3D for Java API непосредственно в ваших проектах Maven с простыми конфигурациями.

Сначала вам нужно указать конфигурацию/местоположение репозитория Aspose `pom.xml`, как показано ниже:

{{< highlight "java" >}}

 <repositories>

    <repository>
        <id>AsposeJavaAPI</id>
        <name>Aspose Java API</name>
        <url>https://releases.aspose.com/java/repo/</url>
    </repository>

</repositories>

{{< /highlight >}}

Затем определите Aspose.3D for Java API зависимость в вашем pom.xml следующим образом:

{{< highlight "java" >}}

 <dependencies>

    <dependency>
        <groupId>com.aspose</groupId>
        <artifactId>aspose-3d</artifactId>
        <version>21.4</version>
    </dependency>

</dependencies>

{{< /highlight >}}

Поздравляем! Вы успешно определили зависимость Aspose.3D for Java Maven в вашем проекте Maven.
