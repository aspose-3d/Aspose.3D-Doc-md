---
title: Аппаратная на основе Рендеринга геометрии 3D
type: docs
weight: 30
url: /ru/python-net/hardware-based-rendering-of-3d-geometry/
description: Используя Aspose.3D для Python via .NET API, разработчики могут запрограммировать графический процессор (блок обработки графики) и настроить графическое оборудование для рендеринга геометрии 3D вместо конвейера фиксированных функций.
---
{{% alert color="primary" %}}

Используя[Aspose.3D для Python via .NET](https://products.aspose.com/3d/python-net/)API, разработчики могут запрограммировать GPU (блок обработки графики) и настроить графическое оборудование для рендеринга геометрии 3D вместо конвейера фиксированных функций. В этой статье мы фокусируемся на аппаратном рендеринге с использованием[OpenGL 4.0](https://www.opengl.org/sdk/docs/man/html/glEnable.xhtml), [DirectX 11](https://msdn.microsoft.com/en-us/library/windows/desktop/hh404489\(v=vs.85\). Aspx),[DirectX 9](https://msdn.microsoft.com/en-us/library/windows/desktop/bb147327\(v=vs.85\). Aspx) и[Вулкан](https://www.khronos.org/registry/vulkan/specs/1.0/xhtml/vkspec.html#VkPipelineRasterizationStateCreateInfo).

{{% /alert %}}
## **Создание аппаратного обеспечения и отмена геометрии 3D**
Чтобы визуализировать геометрию 3D, требуются шейдер, буферы и состояние рендеринга. Никто из них не может работать друг без друга.

- **Буферы**-Треугольные списки-это отдельные треугольники, указанные в массиве, который иногда называют буфером. В списке треугольников каждый треугольник указан индивидуально. Точки треугольника можно совместно использовать с помощью индексов для уменьшения объема данных, которые необходимо передать графическому оборудованию.
- **Шейдеры**-Он определяет, как преобразовать треугольники из мирового пространства в пространство экрана и рассчитать окончательный цвет пикселя на стороне GPU
- **Государства-члены**-Он предоставляет параметры для GPU для растеризации треугольников в пиксели.

{{% alert color="primary" %}}

Мы подготовили демо-проект. Пожалуйста, обратитесь к[Этот URL-адрес загрузки](https://github.com/aspose-3d/Aspose.3D-for-.NET/tree/master/HardwareBasedRendering).

{{% /alert %}}

Язык затенения OpenGL (GLSL)-это стандартный язык затенения высокого уровня для графики OpenGL API. Обычно используются три типа шейдеров: вертикальные шейдеры, фрагментные шейдеры и геометрические шейдеры.

Класс [`GLSLSource`](https://reference.aspose.com/3d/net/aspose.threed.render/glslsource) сообщает рендереру, исходный код предназначен для языка затенения OpenGL, его можно скомпилировать в класс [`ShaderProgram`](https://reference.aspose.com/3d/net/aspose.threed.render/shaderprogram). Класс [`ShaderVariable`](https://reference.aspose.com/3d/net/aspose.threed.render/shadervariable) определяет переменные, используемые в шейдере. Класс `VariableSemantic` используется для идентификации семантической переменной шейдера, рендерер Aspose.3D автоматически подготавливает значения переменной шейдера в зависимости от семантики.
### **Образец программирования для Shader**
Этот пример кода инициализирует рендерер и шейдер для сетки. Вы можете скачать полный рабочий проект этого примера из[Здесь](https://github.com/aspose-3d/Aspose.3D-for-.NET/tree/master/HardwareBasedRendering).

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "HardwareBasedRendering-Controls-RenderView-RenderView.py" >}}
### **Образец программирования для состояния буфера и Рендера**
Этот пример кода инициализирует буфер и состояние рендеринга для сетки.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "HardwareBasedRendering-Grid-ManualEntity.py" >}}
