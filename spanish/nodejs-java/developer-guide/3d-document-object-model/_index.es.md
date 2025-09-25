---
title: Aspose.3D Modelo de Objetos de Documentos (DOM)
type: docs
weight: 20
url: "/es/nodejs-java/aspose-3d-document-object-model"
description: "Cada escena 3D puede comprender cualquier número de ventanas de vista. Utilizando Aspose.3D para la API nodejs-java, los desarrolladores pueden capturar una o más ventanas de vista en una captura de pantalla única. Pueden renderizarla en una aplicación basada en nodejs-java o en una imagen."
---

El Modelo de Objeto 3D (DOM) de Aspose.3D es una representación en memoria potente de una escena 3D. Proporciona a los desarrolladores la capacidad de leer, manipular y modificar el contenido y el formato de una escena 3D programáticamente.

En esta sección, exploraremos las clases clave del DOM de Aspose.3D y sus relaciones. Al utilizar estas clases, puede obtener acceso programático a varios elementos dentro de una escena 3D.

Profundicemos en las clases principales del DOM de Aspose.3D:

* **Escena**: La clase Escena representa la raíz de la jerarquía de la escena 3D. Sirve como contenedor para todos los demás elementos y proporciona métodos para manipular la escena en su conjunto.
* **Nodo**: Los nodos son los componentes básicos de una escena 3D. Representan objetos o entidades individuales dentro de la escena, como mallas, luces, cámaras o grupos. Los nodos se pueden transformar, animar y texturizar.
* **Entidades**: La clase Entidades abarca una amplia gama de objetos y elementos que componen una escena 3D. Incluye entidades como mallas, luces, cámaras, perfiles y más. Estas entidades sirven como componentes básicos, lo que le permite crear escenas complejas combinándolas y manipulándolas programáticamente. La categoría Entidades proporciona acceso y control sobre estos elementos fundamentales de una escena 3D.
* **Materiales**: La clase Materiales se centra en definir las propiedades visuales de los objetos dentro de una escena 3D. Proporciona herramientas para crear, modificar y controlar los materiales de forma programática, que determinan cómo interactúa la luz con las superficies. Al ajustar propiedades como el color, la textura, la transparencia y la reflexión, puede lograr varios efectos visuales y personalizar la apariencia de sus modelos 3D.
* **Animaciones**: La clase Animaciones se centra en crear y controlar el movimiento y las transformaciones dentro de una escena 3D. Le permite definir y manipular animaciones de forma programática, lo que permite que los objetos se muevan, roten, escalen o cambien de propiedades con el tiempo. Con esta categoría, puede agregar elementos dinámicos e interactivos a sus escenas 3D.

Al utilizar las clases del DOM de Aspose.3D mencionadas anteriormente, puede interactuar y manipular programáticamente el contenido y la estructura de una escena 3D. Esto proporciona flexibilidad y control al trabajar con modelos 3D en sus aplicaciones.

## Estructura de la escena

Cuando Aspose.3D lee un archivo 3D en la memoria, genera objetos de varios tipos para representar los diferentes elementos dentro de la escena 3D.

La estructura de la escena en Aspose.3D sigue el patrón de diseño de composición, que ofrece flexibilidad y organización:

* Los nodos sirven como contenedores que pueden contener otros nodos, lo que permite agrupar diferentes objetos dentro de la escena.
* Cada nodo puede tener su propia transformación, que también se aplica a sus nodos hijo.
* Todos los tipos de entidades espaciales en Aspose.3D deben colocarse debajo de una instancia de Nodo. Esto asegura que los objetos como las mallas, las luces, las cámaras y otros elementos estén organizados dentro de la jerarquía de la escena.
* Los nodos pueden contener múltiples materiales, y la relación entre los polígonos y los materiales adjuntos a un nodo se aborda mediante el concepto de `VertexElementMaterial` dentro del objeto Mesh.

![Jerarquía de la escena](scene.png)

## Entidades espaciales
Todas las entidades espaciales en Aspose.3D heredan de la clase `Entity`, sirviendo como componentes básicos para construir entornos virtuales. Aspose.3D categoriza estas entidades en varias categorías principales, cada una con su propio propósito y funcionalidad específicos.

![Entidades](entity.png)

* **Primitivo**: La clase `Primitive` sirve como clase base para todas las geometrías 3D procedimentales dentro de Aspose.3D, como `Cylinder`, `Torus` y `Sphere`. Estas geometrías se pueden definir utilizando un conjunto mínimo de parámetros, lo que facilita la creación de formas 3D básicas.
* **Geometría**: Las geometrías en Aspose.3D típicamente consisten en vértices, aristas y polígonos que definen la forma y la estructura de un objeto 3D. Esta categoría abarca una amplia gama de geometrías complejas utilizadas para representar varios objetos dentro de una escena 3D.
* **Perfil**: Los perfiles, similares a los primitivos, definen contornos cerrados en 2D en el plano x-y. Proporcionan una forma de crear formas 2D que se pueden extruir para generar geometrías 3D correspondientes. Los perfiles se utilizan a menudo como punto de partida para crear objetos 3D más intrincados.
* **Curva**: A diferencia de los perfiles, una curva representa uno o más caminos espaciales que pueden tomar varias formas, como líneas, curvas NURBS o curvas compuestas compuestas por múltiples segmentos de curva. Las curvas se utilizan comúnmente junto con los tipos de extrucción para crear formas 3D dinámicas e intrincadas.
* **Texto**: Aspose.3D incluye la capacidad de generar perfiles a partir de texto utilizando una fuente especificada. Esta función le permite crear perfiles en forma de letras, números o cualquier otro contenido textual, agregando un elemento de personalización o marca a sus modelos 3D.

![Tipos de perfil 2D](profiles.png)

## Tipos de cámara y luz

![Cámara y luz](frustums.png)

## Tipos de material

Aspose.3D proporciona soporte para varios tipos de materiales, que incluyen material Lambert, material Phong, material PBR, material PBR especular y material de sombreador (solo disponible en archivos FBX).

Cada material en Aspose.3D puede tener diferentes atributos y propiedades que definen su apariencia y comportamiento dentro de una escena 3D. Estos materiales se pueden conectar a instancias de textura, mejorando sus características visuales.

Las texturas en Aspose.3D se asocian con un atributo de material específico. El tipo de textura combina las definiciones de parámetros para la fuente de la imagen y el sampler de la textura. Al utilizar texturas, puede aplicar patrones, colores y otros efectos visuales detallados a las superficies de sus modelos 3D.

Con el soporte para una variedad de tipos de materiales y la capacidad de conectar texturas, Aspose.3D ofrece flexibilidad para crear materiales visualmente atractivos y realistas para sus escenas 3D.

![Tipos de material](materials.png)

## Relación de objetos de animación
Aspose.3D proporciona soporte de animación a nivel de datos, y el soporte de cálculo se está desarrollando actualmente.

En Aspose.3D, una escena puede contener múltiples objetos `AnimationClip`. Cada clip de animación puede consistir en múltiples nodos de animación. El nodo de animación sigue el patrón de diseño de composición, lo que permite crear estructuras jerárquicas con subnodos de animación.

Los nodos de animación se pueden asociar con puntos de enlace, que definen las propiedades del objeto de destino que se animarán. Los vectores son tipos de datos comúnmente utilizados en muchas propiedades de entidad. Por lo tanto, los puntos de enlace pueden tener diferentes canales de animación para actualizar canales específicos del vector de forma independiente. Cada canal contiene una secuencia de fotogramas clave que define cómo se anima el valor con el tiempo.

Este sistema proporciona un marco flexible para animar objetos dentro de una escena. Al definir clips de animación, nodos, puntos de enlace y canales, puede crear animaciones complejas y dinámicas que afectan a varias propiedades de las entidades en su escena 3D.

Si bien Aspose.3D actualmente admite la animación a nivel de datos, el desarrollo continuo se centra en ampliar el soporte de cálculo, lo que mejorará las capacidades para crear y manipular animaciones dentro del marco.

![Animaciones](animations.png)

Una escena con animaciones puede tener este tipo de estructura:

![Relaciones de animación](animation_relations.png)