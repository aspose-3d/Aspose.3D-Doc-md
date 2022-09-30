---
title: Добавить свойство анимации и настройку целевой камеры в документе 3D
type: docs
weight: 10
url: /ru/net/add-animation-property-and-setup-target-camera-in-3d-document/
description: В Aspose.3D объектная анимация на самом деле является анимацией ключевого кадра, которая анимирует свойства. Чтобы анимировать свойства, вам нужен экземпляр CurveMapping, который отображает компоненты свойства в разные кривые, например, свойство Vector3 может иметь 3 компонента X/Y/Z, который будет настраивать три канала в CurveMapping, каждый канал может иметь набор Кривые.
---
## **Добавить свойство Animation в документе 3D**
Aspose.3D for .NET поддерживает рендеринг анимированной сцены. Эта статья объясняет предпосылки для перемещения объекта.
### **Положение Move Cube**
{{% alert color="primary" %}}

Объект класса [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh) используется в коде. Мы можем[Создать объект класса Mesh, как там рассказано](/3d/ru/net/create-and-read-an-existing-3d-scene/)И он также должен анимировать свойство локального перевода узла:[Добавление преобразования к узлу](/3d/ru/net/adding-transformation-to-the-node/).

{{% /alert %}}

В Aspose.3D объектная анимация на самом деле является анимацией ключевого кадра, которая анимирует свойства. Чтобы анимировать свойства, вам нужен экземпляр `CurveMapping`, который отображает компоненты свойства в разные кривые, например, свойство `Vector3` может иметь 3 компонента `X`/`Y`/`Z`, которое установит три канала в `CurveMapping`, каждый канал может иметь набор `Curve`.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Animation-PropertyToDocument-AddAnimationPropertyToDocument.cs" >}}
## **Настройка целевой камеры в файле 3D**
Aspose.3D for .NET предлагает настроить целевую камеру в файле 3D. В некоторых форматах файлов свет/камера поддерживает цель, что позволяет свету/камере всегда обращаться к указанному узлу, это полезно в анимации.

{{% alert color="primary" %}}

Классы [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene), [`Camera`](https://reference.aspose.com/3d/net/aspose.threed.entities/camera), [`Node`](https://reference.aspose.com/3d/net/aspose.threed/node) и [`Transform`](https://reference.aspose.com/3d/net/aspose.threed/transform) используются в коде. Чтобы сохранить `Scene`, используется метод [`Scene.Save`](https://reference.aspose.com/3d/net/aspose.threed/scene/methods/save), он принимает имя файла с полным путем и параметром [`FileFormat`](https://reference.aspose.com/3d/net/aspose.threed/fileformat).

{{% /alert %}}

В приведенном ниже примере цель и камера настроены в файле 3D:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-Animation-SetupTargetAndCamera-SetupTargetAndCamera.cs" >}}
