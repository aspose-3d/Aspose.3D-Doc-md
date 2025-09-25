---
title: التثبيت
type: docs
weight: 50
url: /ar/java/installation/
description: تستضيف Aspose جميع واجهات برمجة التطبيقات Java على Aspose Repository. يمكنك بسهولة استخدام Aspose.3D for Java API مباشرةً في مشاريع Maven الخاصة بك مع إعدادات بسيطة.
---

## **تثبيت Aspose.3D لـ Java من مستودع Aspose**

Aspose يستضيف جميع واجهات برمجة التطبيقات Java على [Aspose Repository](https://releases.aspose.com/java/repo/com/aspose/aspose-3d/). يمكنك استخدام Aspose.3D لـ Java مباشرةً في مشاريع Maven الخاصة بك من خلال إعدادات بسيطة.

أولاً تحتاج إلى تحديد تكوين / موقع مستودع Aspose في ملف `pom.xml` الخاص بـ Maven كما هو موضح أدناه:

{{< highlight xml >}}
 <repositories>

    <repository>
        <id>AsposeJavaAPI</id>
        <name>Aspose Java API</name>
        <url>https://releases.aspose.com/java/repo/</url>
    </repository>

</repositories>
{{< /highlight >}}

ثم عرّف اعتماد Aspose.3D لـ Java في ملف pom.xml الخاص بك على النحو التالي:

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

إذا كنت تستخدم JDK-8، يمكنك استخدام نسخة JDK-8 كما يلي:

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

تهانينا! لقد قمت بتعريف اعتماد Aspose.3D لـ Java في مشروع Maven الخاص بك بنجاح.