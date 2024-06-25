---
title: Применение визуальных эффектов при экономии 3D просмотров
type: docs
weight: 10
url: /ru/python-net/apply-visual-effects-on-saving-3d-views/
description: Используя Aspose.3D for Python via .NET API, разработчики могут применять визуальные эффекты к 3D Views перед сохранением изображения. Эти визуальные эффекты также известны как эффекты пост-обработки или фильтры, которые применяются в режиме реального времени ко всему, что отображается в 3D View.
---
{{% alert color="primary" %}}

Используя [Aspose.3D for Python via .NET API](https://products.aspose.com/3d/python-net/), разработчики могут применять визуальные эффекты к 3D Views перед сохранением изображения. Эти визуальные эффекты также известны как эффекты пост-обработки или фильтры, которые применяются в режиме реального времени ко всему, что отображается в 3D View.

{{% /alert %}}
##  **Применение визуальных эффектов на 3D Просмотр**
Метод [`get_post_processing`](https://reference.aspose.com/3d/net/aspose.threed.render/renderer/methods/getpostprocessing) класса [`Renderer`](https://reference.aspose.com/3d/net/aspose.threed.render/renderer) позволяет создать любой поддерживаемый визуальный эффект. Класс `Renderer` предлагает члену [`post_processings`](https://reference.aspose.com/3d/net/aspose.threed.render/renderer/properties/postprocessings) применять различные фильтры, метод Добавить класса `PostProcessings` позволяет включить фильтр перед рендерингом.
###  **Образец программирования**
Этот пример кода применяет визуальный эффект на виде 3D.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "3DViewPorts-ApplyVisualEffects-ApplyVisualEffects.py" >}}
