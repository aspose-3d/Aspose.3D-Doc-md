---
title: Installation
type: docs
weight: 50
url: /zh/java/installation/
description: Aspose 托管 Aspose 存储库中的所有 Java api。您可以通过简单的配置直接在 Maven 项目中使用 Aspose.3D for Java API。
---
##  **正在从 Aspose 存储库安装 Aspose.3D for Java**
Aspose 在 [Aspose 存储库](https://releases.aspose.com/java/repo/com/aspose/aspose-3d/) 上托管所有 Java 个api。您可以通过简单的配置直接在 Maven 项目中使用 Aspose.3D for Java API。

首先，您需要在 Maven `pom.xml` 中指定 Aspose 存储库配置/位置，如下所示:

{{< highlight "xml" >}}

 <repositories>

    <repository>
        <id>AsposeJavaAPI</id>
        <name>Aspose Java API</name>
        <url>https://releases.aspose.com/java/repo/</url>
    </repository>

</repositories>

{{< /highlight >}}

然后在pom.xml中定义 Aspose.3D for Java API 依赖项，如下所示:

{{< highlight "xml" >}}

 <dependencies>

    <dependency>
        <groupId>com.aspose</groupId>
        <artifactId>aspose-3d</artifactId>
        <version>23.11.0</version>
    </dependency>

</dependencies>

{{< /highlight >}}


如果您使用的是JDK-8，则可以使用JDK-8版本，如下所示:

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

恭喜!您已在 Maven 项目中成功定义了 Aspose.3D for Java Maven 依赖项。
