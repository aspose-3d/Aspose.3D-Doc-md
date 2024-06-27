---
title: Добавить свойство анимации и настройку целевой камеры в документе 3D
type: docs
weight: 10
url: /ru/java/add-animation-property-and-setup-target-camera-in-3d-document/
description: Aspose.3D for Java поддерживает рендеринг анимированной сцены. Эта статья объясняет предпосылки для перемещения объекта.
---
##  **Добавить свойство анимации в документе 3D**
Aspose.3D for Java поддерживает рендеринг анимированной сцены. Эта статья объясняет предпосылки для перемещения объекта.
###  **Положение Move Cube**
{{% alert color="primary" %}}

В коде используется объект класса `Mesh`. Мы можем [Создать объект класса Mesh, как там рассказано](https://docs.aspose.com/3d/java/create-3d-mesh-and-scene/), и он также должен анимировать свойство локального перевода узла: [Добавление преобразования к узлу](https://docs.aspose.com/3d/java/adding-transformation-to-the-node/).

{{% /alert %}}

В Aspose.3D for Java API экземпляр анимации на самом деле является анимацией ключевого кадра, которая анимируется в свойствах. Чтобы анимировать свойства, вам нужен экземпляр `CurveMapping`, который отображает компоненты свойства на разные кривые, например, свойство `Vector3` может иметь 3 компонента `X`/`Y`/`Z`, который настроит три канала за `CurveMapping`, каждый канал может иметь набор `Curve`.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-animation-PropertyToDocument-AddAnimationPropertyToDocument.java" >}}
##  **Настройте целевую камеру в файле 3D**
Aspose.3D for Java предлагает настроить целевую камеру в файле 3D. В некоторых форматах файлов свет/камера поддерживает цель, что позволяет свету/камере всегда смотреть на указанный узел, это полезно в анимации.

{{% alert color="primary" %}}

В коде используются классы `Scene`, `Camera`, `Node` и `Transform`. Чтобы сэкономить `Scene`, используется метод `Scene.save`, он принимает имя файла с полным путем и параметром `FileFormat`.

{{% /alert %}}

В примере ниже цель и камера настроены в файле 3D:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-animation-SetupTargetAndCamera.java" >}}
