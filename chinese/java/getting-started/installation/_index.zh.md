---
title: 安装
type: docs
weight: 50
url: /zh/java/installation/
description: Aspose 在 Aspose Repository 上托管所有 Java API。您可以通过简单的配置，在 Maven 项目中直接轻松使用 Aspose.3D for Java API。
---

## **从 Aspose Repository 安装 Aspose.3D for Java**

Aspose 将所有 Java API 托管在 [Aspose Repository](https://releases.aspose.com/java/repo/com/aspose/aspose-3d/) 上。您可以通过简单的配置，在 Maven 项目中直接使用 Aspose.3D for Java API。

首先，需要在 Maven 的 `pom.xml` 中指定 Aspose Repository 的配置/位置，如下所示：

{{< highlight xml >}}

 <repositories>

    <repository>
        <id>AsposeJavaAPI</id>
        <name>Aspose Java API</name>
        <url>https://releases.aspose.com/java/repo/</url>
    </repository>

</repositories>

{{< /highlight >}}

然后在 `pom.xml` 中定义 Aspose.3D for Java API 的依赖，如下所示：

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

如果您使用的是 JDK‑8，可以使用带有 JDK‑8 分类器的版本，示例如下：

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

恭喜！您已成功在 Maven 项目中定义 Aspose.3D for Java 的 Maven 依赖。