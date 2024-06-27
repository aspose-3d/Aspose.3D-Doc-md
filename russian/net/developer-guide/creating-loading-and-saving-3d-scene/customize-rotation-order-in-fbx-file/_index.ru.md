---
title: Настройте порядок ротациив файле FBX
type: docs
weight: 10
url: /ru/net/customize-rotation-order-in-fbx-file
description: Используя Aspose.3D for .NET, разработчики могут настроить собственные свойства FBX, такие как RotationOrder.
---
{{% alert color="primary" %}}

Используя [Aspose.3D for .NET](https://products.aspose.com/3d/net/), иногда разработчики требуют точного контроля над функциями, специфичными для формата, такими как изменение `RotationOrder` в экспортере FBX. Хотя API, непосредственно раскрывающие эту функциональность, может и не быть общедоступным, Aspose.3D for .NET предоставляет способы достижения таких настроек благодаря своей гибкой архитектуре.
{{% /alert %}}



Вот как вы можете справиться с этим в Aspose.3D:

{{% highlight "csharp" %}}

var rvm = Scene.FromFile(@"F1234.rvm");
rvm.RootNode.Accept((Node node) =>
{
    node.SetProperty("RotationOrder", 1); //set a custom property, exporter will match this to FBX's property.
    return true; //continue to traverse on other nodes 
});

rvm.Save(@"test.fbx");

{{% /highlight %}}

В этом примере:

1. Создайте сцену из файла RVM.
1. Посетите все узлы в сцене.
1. Set custom property: Метод SetProperty используется для установки свойства `RotationOrder`, демонстрируя, как можно использовать внутренние механизмы для управления специфическими для формата функциями, которые не представлены напрямую общественности API.
1. Сохранить сцену: сцена сохраняется с настроенным `RotationOrder`.

Используя такие методы, Aspose.3D позволяет разработчикам точно настраивать и контролировать специфические функции форматов 3D, гарантируя, что подробные и точные требования будут выполнены в различных приложениях 3D.