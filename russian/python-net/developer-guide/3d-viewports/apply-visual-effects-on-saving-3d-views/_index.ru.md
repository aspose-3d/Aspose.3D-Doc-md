---
title: Применить визуальные эффекты при сохранении просмотров 3D
type: docs
weight: 10
url: /ru/python-net/apply-visual-effects-on-saving-3d-views/
description: Используя Aspose.3D для Python via .NET API, разработчики могут применять визуальные эффекты на 3D Просмотры перед сохранением в изображении. Эти визуальные эффекты также известны как эффекты постобработки или фильтры, которые применяются в режиме реального времени ко всему, что отображается в представлении 3D.
---
{{% alert color="primary" %}}

Используя[Aspose.3D для Python via .NET 0761234881](https://products.aspose.com/3d/python-net/), Разработчики могут применять визуальные эффекты на 3D Views перед сохранением в изображении. Эти визуальные эффекты также известны как эффекты постобработки или фильтры, которые применяются в режиме реального времени ко всему, что отображается в представлении 3D.

{{% /alert %}}
## **Применить визуальные эффекты на 3D View**
Метод [`get_post_processing`](https://reference.aspose.com/3d/net/aspose.threed.render/renderer/methods/getpostprocessing) класса [`Renderer`](https://reference.aspose.com/3d/net/aspose.threed.render/renderer) позволяет создавать любой поддерживаемый визуальный эффект. Класс `Renderer` предлагает член [`post_processings`](https://reference.aspose.com/3d/net/aspose.threed.render/renderer/properties/postprocessings) для применения различных фильтров, метод Add класса `PostProcessings` позволяет включать фильтр перед рендерингом.
### **Образец программирования**
Этот пример кода применяет визуальный эффект на представлении 3D.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "3DViewPorts-ApplyVisualEffects-ApplyVisualEffects.py" >}}
