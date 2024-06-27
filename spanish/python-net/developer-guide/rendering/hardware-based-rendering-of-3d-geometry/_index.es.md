---
title: Renderización basada en hardware de geometría 3D
type: docs
weight: 30
url: /es/python-net/hardware-based-rendering-of-3d-geometry/
description: Usando Aspose.3D for Python via .NET API, los desarrolladores pueden programar la GPU (unidad de procesamiento de gráficos) y configurar el hardware de gráficos para renderizar la geometría 3D en lugar de la canalización de función fija.
---
{{% alert color="primary" %}}

Usando [Aspose.3D for Python via .NET](https://products.aspose.com/3d/python-net/) API, los desarrolladores pueden programar la GPU (unidad de procesamiento de gráficos) y configurar el hardware de gráficos para renderizar la geometría 3D en lugar de la canalización de función fija. En este artículo, nos centramos en la representación basada en hardware utilizando [OpenGL 4,0](https://www.opengl.org/sdk/docs/man/html/glEnable.xhtml), [DirectX 11](https://msdn.microsoft.com/en-us/library/windows/desktop/hh404489\(v=vs.85\).aspx), [DirectX 9](https://msdn.microsoft.com/en-us/library/windows/desktop/bb147327\(v=vs.85\).aspx y [Vulkan](https://www.khronos.org/registry/vulkan/specs/1.0/xhtml/vkspec.html#VkPipelineRasterizationStateCreateInfo).

{{% /alert %}}
##  **Crear hardware y render una geometría 3D**
Para renderizar una geometría 3D, se requiere un shader, buffers y un estado de render. Ninguno de ellos puede trabajar el uno sin el otro.

- **Tampones**-Las listas de triángulos son triángulos individuales especificados en una matriz que a veces se denomina búfer. En una lista de triángulos, cada triángulo se especifica individualmente. Los puntos de un triángulo se pueden compartir mediante índices para reducir la cantidad de datos que se deben pasar al hardware gráfico.
- **Shaders**-Define cómo transformar los triángulos del espacio del mundo en el espacio de la pantalla y calcular el color del píxel final en el lado de la GPU
- **Estados de render**-Proporciona parámetros para que la GPU rasterice los triángulos en píxeles.

{{% alert color="primary" %}}

Hemos preparado un proyecto de demostración. Por favor refiérase a [Esta URL de descarga](https://github.com/aspose-3d/Aspose.3D-for-.NET/tree/master/HardwareBasedRendering).

{{% /alert %}}

El Lenguaje de Sombreado OpenGL (GLSL) es el lenguaje estándar de sombreado de alto nivel para los gráficos OpenGL API. Hay tres tipos de sombreadores comúnmente utilizados: Vertex Shaders, Fragment Shaders y Geometry Shaders.

La clase [`GLSLSource`](https://reference.aspose.com/3d/net/aspose.threed.render/glslsource) le dice al renderizador, el código fuente es para el lenguaje de sombreado OpenGL, se puede compilar a la clase [`ShaderProgram`](https://reference.aspose.com/3d/net/aspose.threed.render/shaderprogram). La clase [`ShaderVariable`](https://reference.aspose.com/3d/net/aspose.threed.render/shadervariable) define las variables utilizadas en el shader. La clase `VariableSemantic` se usa para identificar la semántica de la variable de sombreado, Aspose.3D El renderizador preparará automáticamente los valores de la variable de sombreado según la semántica.
###  **Muestra de programación para Shader**
Este ejemplo de código inicializa el renderizador y el sombreador para la cuadrícula. Puede descargar el proyecto de trabajo completo de este ejemplo desde [Aquí](https://github.com/aspose-3d/Aspose.3D-for-.NET/tree/master/HardwareBasedRendering).

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "HardwareBasedRendering-Controls-RenderView-RenderView.py" >}}
###  **Muestra de programación para el búfer y el estado de renderización**
Este ejemplo de código inicializa el búfer y el estado de procesamiento para la cuadrícula.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "HardwareBasedRendering-Grid-ManualEntity.py" >}}
