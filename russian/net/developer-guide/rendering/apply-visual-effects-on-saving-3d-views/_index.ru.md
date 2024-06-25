---
title: Применение визуальных эффектов при экономии 3D просмотров
type: docs
weight: 10
url: /ru/net/apply-visual-effects-on-saving-3d-views/
description: Используя Aspose.3D for .NET API, разработчики могут применять визуальные эффекты к 3D Views перед сохранением изображения. Эти визуальные эффекты также известны как эффекты пост-обработки или фильтры, которые применяются в режиме реального времени ко всему, что отображается в 3D View.
---
{{% alert color="primary" %}}

Используя [Aspose.3D for .NET API](https://products.aspose.com/3d/net/), разработчики могут применять визуальные эффекты к 3D Views перед сохранением изображения. Эти визуальные эффекты также известны как эффекты пост-обработки или фильтры, которые применяются в режиме реального времени ко всему, что отображается в 3D View.

{{% /alert %}}
##  **Применение визуальных эффектов на 3D Просмотр**
Метод [`GetPostProcessing`](https://reference.aspose.com/3d/net/aspose.threed.render/renderer/methods/getpostprocessing) класса [`Renderer`](https://reference.aspose.com/3d/net/aspose.threed.render/renderer) позволяет создать любой поддерживаемый визуальный эффект. Класс Renderer предлагает член [`PostProcessings`](https://reference.aspose.com/3d/net/aspose.threed.render/renderer/properties/postprocessings) для применения различных фильтров, метод Add класса PostProcessings позволяет включить фильтр перед рендерингом.
###  **Образец программирования**
Этот пример кода применяет визуальный эффект на виде 3D.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-3DViewPorts-ApplyVisualEffects-ApplyVisualEffects.cs" >}}
