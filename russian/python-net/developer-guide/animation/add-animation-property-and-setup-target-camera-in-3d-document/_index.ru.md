---
title: Добавить свойство анимации и настройку целевой камеры в документе 3D
type: docs
weight: 10
url: /ru/python-net/add-animation-property-and-setup-target-camera-in-3d-document/
description: В Aspose.3D объектная анимация на самом деле является ключевой анимацией кадра, которая анимируется в свойствах. Чтобы анимировать свойства, вам нужен экземпляр CurveMapping, который отображает компоненты свойства на различные кривые, например, свойство Vector3 может иметь 3 компонента X/Y/Z, которые будут настраивать три канала в CurveMapping, каждый канал может иметь набор кривых.
---
##  **Добавить свойство анимации в документе 3D**
Aspose.3D for Python via .NET поддерживает рендеринг анимированной сцены. Эта статья объясняет предпосылки для перемещения объекта.
###  **Положение Move Cube**
{{% alert color="primary" %}}

В коде используется объект класса [`Mesh`](https://reference.aspose.com/3d/net/aspose.threed.entities/mesh). Мы можем [Создать объект класса Mesh, как там рассказано](/3d/ru/net/create-and-read-an-existing-3d-scene/), и он также должен анимировать свойство локального перевода узла: [Добавление преобразования к узлу](/3d/ru/net/adding-transformation-to-the-node/).

{{% /alert %}}

В Aspose.3D объектная анимация на самом деле является ключевой анимацией кадра, которая анимируется в свойствах. Чтобы анимировать свойства, вам нужен экземпляр `CurveMapping`, который отображает компоненты свойства на разные кривые, например, свойство `Vector3` может иметь 3 компонента `X`/`Y`/`Z`, который настроит три канала за `CurveMapping`, каждый канал может иметь набор `Curve`.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Animation-PropertyToDocument-AddAnimationPropertyToDocument.py" >}}
##  **Настройте целевую камеру в файле 3D**
Aspose.3D for Python via .NET предлагает настроить целевую камеру в файле 3D. В некоторых форматах файлов свет/камера поддерживает цель, что позволяет свету/камере всегда смотреть на указанный узел, это полезно в анимации.

{{% alert color="primary" %}}

В коде используются классы [`Scene`](https://reference.aspose.com/3d/net/aspose.threed/scene), [`Camera`](https://reference.aspose.com/3d/net/aspose.threed.entities/camera), [`Node`](https://reference.aspose.com/3d/net/aspose.threed/node) и [`Transform`](https://reference.aspose.com/3d/net/aspose.threed/transform). Для сохранения сцены используется метод [`Scene.Save`](https://reference.aspose.com/3d/net/aspose.threed/scene/methods/save), который принимает имя файла с полным путем и параметром [`FileFormat`](https://reference.aspose.com/3d/net/aspose.threed/fileformat).

{{% /alert %}}

В примере ниже цель и камера настроены в файле 3D:

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Animation-SetupTargetAndCamera-SetupTargetAndCamera.py" >}}
