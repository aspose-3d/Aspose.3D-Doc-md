---
title: Добавить свойство анимации и настройку целевой камеры в документе 3D
type: docs
weight: 10
url: /ru/java/add-animation-property-and-setup-target-camera-in-3d-document/
description: Aspose.3D for Java поддерживает рендеринг анимированной сцены. Эта статья объясняет предпосылки для перемещения объекта.
---
## **Добавить свойство Animation в документе 3D**
Aspose.3D for Java поддерживает рендеринг анимированной сцены. Эта статья объясняет предпосылки для перемещения объекта.
### **Положение Move Cube**
{{% alert color="primary" %}}

Объект класса `Mesh` используется в коде. Мы можем[Создать объект класса Mesh, как там рассказано](https://docs.aspose.com/3d/java/create-3d-mesh-and-scene/)И он также должен анимировать свойство локального перевода узла:[Добавление преобразования к узлу](https://docs.aspose.com/3d/java/adding-transformation-to-the-node/).

{{% /alert %}}

В Aspose.3D for Java API экземпляр анимации на самом деле является анимацией ключевого кадра, которая анимирует свойства. Для того, чтобы анимировать свойства, вам нужен экземпляр `CurveMapping`, который отображает компоненты свойства в разные кривые, например, свойство `Vector3` может иметь 3 компонента `X`/`Y`/`Z`, которое установит три канала в `CurveMapping`, каждый канал может иметь набор `Curve`.

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "src-java-examples-animation-PropertyToDocument-AddAnimationPropertyToDocument.java" >}}
## **Настройка целевой камеры в файле 3D**
Aspose.3D for Java предлагает настроить целевую камеру в файле 3D. В некоторых форматах файлов свет/камера поддерживает цель, что позволяет свету/камере всегда обращаться к указанному узлу, это полезно в анимации.

{{% alert color="primary" %}}

Классы `Scene`, `Camera`, `Node` и `Transform` используются в коде. Для сохранения `Scene` используется метод `Scene.save`, он принимает имя файла с полным путем и параметром `FileFormat`.

{{% /alert %}}

В приведенном ниже примере цель и камера настроены в файле 3D:

{{< gist "aspose-3d-gists" "50e7f479a64956c0bf78841c0799ba76" "aspose-3d-src-examples-animation-SetupTargetAndCamera.java" >}}
